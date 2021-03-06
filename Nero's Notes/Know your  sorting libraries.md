# Know your sorting libraries

To sort an array, use Arrays.sort(A), and to sort a list use Collections.sort(list).
- The time complexity of Arrays.sort(A) is O(n log n), where n is the length of the array A. The space complexity is as high as n/2 objects references for randomly ordered input arrays. For nearly sorted inputs, both time and space complexity are much better: approximately n comparisons, and constant space.
- Arrays.sort(A) operates on arrays of objects that implements the Comparable interface. Collections.sort(list) does the same on lists.
- Both Arrays.sort(A, cmp) and Collections.sort(list, cmp) have the provision of sorting according to an explicit comparator object.
- Collections.sort(L) internally proceeds by forming an array A, calling Arrays.sort(A) on that array, and then writing the result back into the list L. this implies that the time complexity of Collections.sort(L) is the same as that of Arrays.sort(A). Because of the copy, the space complexity is always O(n). In particular, Collections.sort(L) applied to a LinkedList has O(n log n ) time complexity.