Searching is a very broad concept, and it is present in many data structures. For example, `contains(e)` is present in `ArrayList, LinkedList, HashSet` and `TreeSet`, albeit with very different time complexities. Here we focus on binary search.

- To search an array, use `Arrays.binarySearch(A, "Euler")` . The time complexity is O(log(n)), where n is the length of the array.
- To search a sorted list-type object, use `Collections.binarySearch(list, 42)`. These return the index of the searched key if it is present, and a negative value if it is not present. 
- The time complexity depends on the nature of the list implementation. For ArrayList (and more generally, any list implementation in which positional access is constant time), it is O(log(n)), where n is the number of elements in the list. For LinkedList it is O(n).
- When there are multiple occurrences of the search key, neither Arrays nor Collections offer any guarantees as to which one will be found by binary search.
- If the search key is not present, both methods return (- (insertion point) -1), where insertion point is defined as the point at which the key would be inserted into the array, i.e, the index of the first element greater than the key, or the number of elements if all elements are less than the specified value.


