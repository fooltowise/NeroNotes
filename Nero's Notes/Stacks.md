# Stacks

A *Stack* supports two basic operations - push and pop. Elements are added (pushed) and removed (popped) in last in, first out order. If the stack is empty, pop typically returns null or throws an exception.

When the stack is implemented using a linked list these operations have O(1) time complexity. If its is implemented using an array, there is a maximum number of entries it can have, but push and pop are still O(1). If the array is dynamically resized, the amortized time for both push and pop is O(1). A stack can support additional operations such as peek, which returns the top of the stack without popping it. 

Learn to recognize when the stack **LIFO** property is applicable, For example, parsing typically benefits from a stack. 

Consider augmenting the basic stack or queue data structure to support additional operations, such as finding the maximum element.

[[Know your stack libraries]]
