# Learn your Queue libraries
The preferred way to manipulate queues is via the Deque interface. The LinkedList class is a doubly linked list that implements this interface, and provides efficient O(1) time queue and stack functionality.

The key queue-related methods in the Deque interface are:
- addLast(3.14)
- removeFirst()
- getFirst()
- offerLast(3.14)
- pollFirst()
- peekFirst()
- addLast(3.14) enqueues an element. Some classes implementing Deque have capacity limits and/or preclude null from being enqueued, but this is not the case for LinkedList.
- removeFirst() retrieves and removes the first element of the Deque, throwing NoSuchElementException if the deque is empty.
- getFirst() retrieves, but does not remove, the first element of this deque, throwing NoSuchElementException if the deque is empty.

The methods offerLast('a'), pollFirst() and peekFirst() are very similar to addLast('a'), removeFirst() and getFirst(), the exception being that they are less prone to throwing exceptions. For example, if the queue is at full capacity, offerLast returns false, indicating the enqueue was unsuccessful. Both pollFirst() and peekFirst() return null if the queue is empty. This can be ambiguous if null is a valid entry.

Other useful queue related methods are Iterator() and descendingIterator().

