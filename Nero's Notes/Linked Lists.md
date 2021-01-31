# Linked Lists

A *singly linked list* is a data structure that contains a sequence of nodes such that each node contains an object and a reference to the next node in the list. The first node is referred to as the *head* and the last node is referred to as the *tail*; the tail's next field is null. There are many variants of linked lists, e.g, in a *doubly linked list*, each node has a link to its predecessor; similarly, a sentinel node or a self-loop can be used instead of null. 

Insert and delete nodes are local operations and have O(1) time complexity. Search requires traversing the entire list, e.g if the key is at the last node or is absent, so it's time complexity is O(n) where n is the number of nodes.

- List problems often have a simple brute-force solution that uses O(n) space, but a subtler solution that uses the existing list nodes to reduce space complexity to O(1).
- Very often, a problem on lists is conceptually simple, and is more about cleanly coding what's specified, rather than designing an algorithm. 
- Consider using a dummy head (sometimes referred to as a sentinel) to avoid having to check for empty lists. This simplifies code, and makes bugs less likely.
- It's easy to forget to update next (and previous for double linked list) for the head and tail.
- Algorithms operating on singly linked lists often benefit from using two iterators, one ahead of the other, or one advancing quicker than the other. 


- Know your [[Java Linked List libraries]]
