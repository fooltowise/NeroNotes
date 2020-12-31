The preferred way to represent stacks in Java is via the Deque interface. The LinkedList class is a doubly linked list that implements this interface, and provides efficient O(1) time stack and queue functionality.
The key stack-related methods in the Deque interface are:
- push(42)
- peek()
- pop().

The Deque methods addFirst(), peekFirst() and removeFirst() are identical to push, peek and pop. We use them in our solutions in place of push, peek and pop.
- push(e) pushes an element onto the stack. Not much can go wrong with a call to push: some implementing classes may throw an IllegalStateException if the capacity is exceeded, or a NullPointerException if the element being inserted is null. LinkedList has no capacity limit and allows for null entries, though as we will see you should be very careful when adding null.
- peek() will retrieve, but does not remove, the element at the top of the stack. If the stack is empty, it returns null. Since null may be a valid entry, this leads to ambiguity. Therefore a better test for an empty stack is IsEmpty().
- pop() will remove and return the element at the top of the stack. It throws NoSuchElementException if the deque is empty. To avoid the exception, first test with IsEmpty().

Other useful stack-related methods are descendingIterator() and iterator().


