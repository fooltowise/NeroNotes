# Heaps

A *heap* is a specialized [[Binary Trees]]. Specifically, it is a complete binary tree. The keys must satisfy the *heap property* - the key at each node is at least as great as the keys stored at its children. A max-heap can be implemented as an array; the children of the node at index *i* are at indices *2i+1* and *2i +2*.

A max-heap supports O(log n) insertions, O(1) time lookup for the max element, and O(log n) deletion of the max element. The extract-max operation is defined to delete and return the maximum element. 

A heap is sometimes defined to as a priority queue because it behaves like a queue, with one difference: each element has a "priority" associated with it, and deletion removes the element with the highest priority.

The *min-heap* is a completely symmetric version of the data structure and supports O(1) time for look-ups for the minimum element.

- Use a heap when **all you care about** is **the largest or smallest elements**, and you do not need to support fast lookup, delete, or search operations for arbitrary elements.
- A heap is a good choice when you need to compute the **k largest or smallest** elements in a collection. For the former, use a min-heap, for the latter, use a max-heap


[[Know your heap libraries]]

