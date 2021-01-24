A hash table is a data structure used to store keys, optionally, with corresponding values. Inserts, deletes and lookups run in O(1) time on average.

The underlying idea is to store keys in an array. A key is stored in the array locations ("slots") based on its "hash code". The hash code is an integer computed from the key by a hash function. If the has function is chosen well, the objects are distributed uniformly across the array locations.

If two keys map to the same location, a "collision" is said to occur. The standard mechanism to deal with collisions is to maintain a linked list of objects at each array location. If the hash function does a good job of spreading objects across the underlying array and take O(1) time to compute, on average, lookups, insertions, and deletions have O(1 + n/m)  time complexity, where n is the number of objects and m is the length of the array. If the "load" n/m  grows large, rehashing can be applied to the hash table. A new array with a larger number of locations is allocated, and the objects are moved to the new array. Rehashing is expensive (O(n+m) time) but if it is done infrequently (for example, whenever the number of entries doubles), its amortized cost is low.

A hash table is qualitatively different from a sorted array - keys do not have to appear in order, and randomization (specifically, the hash function) plays a central role. Compared to binary search trees, inserting and deleting in a hash table is more efficient (assuming rehashing is infrequent). One disadvantage of hash tables is the need for a good hash function but this is rarely an issue in practice. Similarly, rehashing is not a problem outside of real-time systems and even for such systems, a separate thread can do the rehashing.

A hash function has one hard requirement: equal keys should have equal codes. This may seem obvious, but is easy to get wrong, e.g, by writing a hash function that is based on address rather than content, or by including profiling data.

A softer requirement is that a hash function should "spread" keys, i.e, the hash codes for a subset of objects should be uniformly distributed across the underlying array. In addition, a hash function should be efficient to compute.

A common mistake with hash tables is that a key that's present in a hash table will be updated. The consequence is that a lookup for that key will now fail, even though it's still in the hash table. If you have to update a key, first remove it, then update it, and finally, add it back - this ensures it's moved to the correct array location. As a rule, you should avoid using mutable objects as keys.

Now we illustrate the steps for designing a hash function suitable for strings. First, the hash function should examine all the characters in the string. It should give a large range of values, and should not let one character dominate (e.g, if we simply cast characters to integers and multiplied them, a single 0 would result in a hash code of 0). We would also like a rolling hash function, one in which if a character is deleted from the front of the string, and another added to the end, the new hash code can be computed in O(1) time. The following function has these properties:

```java
public static int stringHash(String s, int modulus){
 	final int MULT  =  997;
 	return s.chars().reduce(0, (val, c) -> (val * MULT * + c) % modulus);
}
```

A hash table is a good data structure to represent a dictionary, i.e, a set of strings. In some applications, a trie, which is a tree data structure that is used to store a dynamic set of strings, has computational advantages. Unlike a BST, nodes in the tree do no store a key. Instead, the node's key position in the tree defines the key which it is associated with.


### Hash Tables boot camp
We introduce hash tables with two examples - one is an application that benefits from the algorithmic advantages of hash tables, and the other illustrates the design of a class that can be used in a hash table.

#### An application of hash tables

Anagrams are popular word play puzzles, whereby rearranging letters of one set of words, you get another set of words. For example, "eleven plus two" is an anagram for "twelve plus one". Crossword puzzles enthusiasts and Scrabble players benefit from the ability to view all possible anagrams of a given set of letters.

Suppose you were asked to write a program that takes as input a set of words and returns groups of anagrams for those words. Each group must contain at least two words.

For example, if the input is "debitcard", "elvis", "silent", "badcredit", "lives", "freedom", "listen", "levis", "money", then there are three groups of anagrams: (1)  "debitcard",  "badcredit"; (2) "elvis", "lives", "levis"; (3) "silent", "listen".

Let's begin by considering the problem of testing whether one word is an anagram of another. Since anagrams do not depend on the ordering of characters in the strings, we can perform the test by sorting the characters in the string. Two words are anagrams if and only if  they result in equal strings after sorting. For example, sort("logarithmic") and sort("algorithmic")  are both "acghiilmort", so "logarithmic" and "algorithmic" are anagrams.

We can form the described grouping of strings by iterating through all strings, and comparing each string with all other remaining strings. If two strings are anagrams, we do not consider the second string again. This leads to an O(n^2  m log m) algorithm, where n is the number of strings and m is the maximum strong length.

Looking more carefully at the above computation, note that the key idea is to map strings to a representative. Given any string, its sorted version can be used as a unique identifier for the anagram group it belongs to. What we want is a map  from a sorted  string to the anagrams it corresponds to.  Anytime you need to store a set of strings, a hash table is an excellent choice. Our final algorithm proceeds by adding sort(s) for each string s in the dictionary to a hash table. The sorted strings are keys, and the values are arrays of the corresponding strings from the original input.

```java
public static List<List<String>> findAnagrams(List<String> dictionary){
		Map<String, List<String>> sortedStringToAnagrams = new HashMap<>();
		for (String s : dictionary){
			String sortedStr = Stream.of(s.split("")).sorted().collect(Collectors.joining());
			sortedStringToAnagrams.putIfAbsent(sortedStr, new ArrayList<String>());
			sortedStringToAnagrams.get(sortedStr).add(s);
		}
		return sortedStringToAnagrams.values()
			.stream()
			.filter(group -> group.size()>=2)
			.collect(Collectors.toList());
}
```


The computation consists of n calls to sort and n insertions into the hash table. Sorting all the keys has time complexity O(nm log m)). The insertions add a time complexity O(nm), yielding O(nm log m) time complexity in total.


#### Design of a hash table class

Consider a class that represents contacts. For simplicity, assume each contact is a string. Suppose it is a hard requirement that the individual contacts are to be stored in a list and it's possible that the list contains duplicates. Two contacts should be equal id they contain the same set of strings, regardless of the ordering of the strings within the underlying list. Multiplicity is not important, i.e, three repetitions of the same contact is the same as a single instance of that contact. In order to be able to store contacts in a hash table, we first need to explicitly define equality, which we can do by forming sets from the lists and comparing the sets.

In our context, this implies that the hash function should depend on the strings present, but not their ordering; it should also consider only one copy if a string appears in duplicate form. We do this by forming a set from the list, and calling the hash function for the set. The library hash function for sets is order-independent, and a set automatically suppress duplicates, so this hash function meets our requirements. It should be pointed out that the hash function and equals methods below are very inefficient. In practice, it would be advisable to cache the underlying set and the hash code, remembering to void these values on updates.

```java
public static List<ContactList> mergeContactLists(List<ContactList> contacts){
	return new ArrayList<>(new Hashset(contacts));
}

public static class ContactList{
	public List<String> names;
	
	public ContactList(List<String> names){this.names = names;}
	
	@Override
	public boolean equals(Object obj){
		if (obj == null || !(obj instanceof ContactList)) return false;
		return this == obj || new HashSet(names).equals( new HashSet(((ContactList)obj).names));
	}
	
	@Override
	public int hashCode(){
	 	return new HashSet(names).hashCode();
	}
}
```
The time complexity of computing the hash is O(n), where n is the number of strings in the contact list. Hash codes are often cached for performance, with the caveat that the cache must be cleared if object fields that are referenced by the hash function are updated.


### Top tips for hash tables
- Hash tables have the best theoretical and real-world performance for lookup, insert and delete. Each of these operations has O(1) time complexity. The O(1) time complexity for insertion is for the average case - a single insert can take O(n) if the hash table has to be resized.
-   Consider using a hash code as a signature to enhance performance, e.g to filter out candidates.
-   Consider using a pre-computed lookup table instead of boilerplate if-then code for mappings, e.g, from character to value, or character to character.
-   When defining your own type that will be put in a hash table, be sure you understand the relationship between logical equality and the fields the hash function must inspect. Specifically, anytime equality is implemented, it is imperative that the correct hash function is also implemented, otherwise when objects are placed in hash tables, logically equivalent objects may appear in different buckets, leading to lookups returning false, even when the searched item is present.
-   Sometimes you will need a multi-map, i.e a map that contains multiple values for a single key, or a bi-directional map. If the language's standard libraries do not provide the functionality you need, learn how to implement a multi-map using lists as values, or find a third party library that has a multi-map.

[[Know your hash table libraries]]




