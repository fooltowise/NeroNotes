There are two hash table-based data structures commonly used in Java - HashSet and HashMap. The difference between the two is that the latter stores key-value pairs, while the former simply stores keys. Both have the property that they do not allow for duplicate keys, unlike, for example, LinkedList and PriorityQueue. Technically, HashSet implements the Set interface, while HashMap implements the Map interface.

The most important methods for HashSet are methods defined in Set:
- add(144)
- remove("cantor")
- contains(24)
- iterator()
- isEmpty()
- size()

Both add(144) and remove("cantor") return a boolean if the added/removed element was already present. It's important to remember that null is a valid entry.

The order in which keys are traversed  by the iterator returned by iterator() is unspecified; it may even change with time. The class LinkedHashSet sub-classes HashSet - the only difference is that iterator() returns keys in the order in which they were inserted into the set. This order is not affected if an element is re-inserted into the set, i.e, if s.add(x) is called when s.contains(x) is true.

HashSet implements retainAll(C), which can be used to perform set intersection - this can be used to reduce coding burden substantially in some cases. A related method is removeAll(C).


The most important methods for HashMap are methods defined in Map:
- put('z', 36)
- get("Hardy")
- remove('z')
- containsKey("Hardy")

There are several methods that are relevant for iteration:
- entrySet()
- keySet()
- valueSet(), and values().

Note that these methods do not follow a parallel naming scheme. The generic static inner class Map.Entry<K,V> is used to iterate over key-value pairs. Iteration order is not fixed - though iteration over the entry set, the key set, and the value set does match up.

To iterate in fixed order, use a LinkedHashMap. A LinkedHashMap is somewhat more complex than a LinkedHashSet - for example, it can be specified that the iteration should proceed in insertion order, or in access order (in which case a call to get(42) will move the corresponding element to the front of the ordering). A LinkedHashMap can also specify capacity constraints, and enable a least-recently used eviction policy.

The Objects class provides a number of static utility methods that can greatly reduce the burden of writing equals(obj) and hashCode(). Example methods include Objects.equals(x,y), Objects.deepEquals(A,B) and Objects.hash(42, "Douglas Adams", 3.14, new Date()).




