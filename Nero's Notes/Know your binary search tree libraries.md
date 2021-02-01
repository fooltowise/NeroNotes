# Know your Binary Search Tree libraries

There are two BST-based data structures commonly used in Java - TreeSet and TreeMap. The former implements the Set interface, and the latter implements the Map interface.

The sortedness of the keys in a BST means that TreeSet and TreeMap have functionality beyond that specified by Set and Map. First, we describe the functionalities added by TreeSet:
- The iterator returned by iterator() traverses keys in ascending order. To iterate over keys in descending order, use descendingIterator()
- first()/last() yield the smallest and largest keys in the tree.
- lower(12)/higher(3) yield the largest element strictly less than the argument/smallest element strictly greater than the argument.
- floor(4.9)/ceiling(5.7) yield the largest element less than or equal to the argument/smallest element greater than or equal to the argument
- headSet(10), tailSet(5), subSet(1,12) return views of the portion of the keys lying in the given range. It's particularly important to note that these operations take O(log n) time, since they are backed by the underlying tree. This implies changes to the tree may change the view. It also means that operations like size() have O(n) time complexity.

As always, there are subtleties, e.g how does first() handle an empty tree, what happens if lower() is called with null, is the range in subSet() inclusive, etc.

The functionalities added by TreeMap are similar, e.g, floorKey(12) is analogous to floor(12), headMap(20) is analogous to headSet(20).

The TreeSet and TreeMap constructors permit for an explicit comparator object that is used to order keys, and you should be comfortable with the syntax used to specify this object.
