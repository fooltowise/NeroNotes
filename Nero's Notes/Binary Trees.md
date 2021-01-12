 A *Binary Tree* is a data structure that is useful for representing hierarchy. Formally, a binary tree is either empty, or a *root* node *r* together with a left binary tree and a right binary tree. The subtrees themselves are binary trees. The left binary tree is sometimes referred to as the left subtree of the root, and the right binary tree is referred to as the right subtree of the root.
 
 Often the node stores additional data. Each node, except the rood, is itself the root of a left subtree or a right subtree. If *l* is the root of *p*''s left subtree, we will say *l* is the *left child* of *p*, and *p* is the *parent* of *l*; the notion of *right child* is similar. If a node is a left or a right child of *p*, we say that it is a *child* of *p*. Note that with the exception of the root, every node has an unique parent. Usually, but not universally, the node object definition includes a parent field (which is null for the root). Observe that for any node there exists a unique sequence of nodes from the root to that node with each node in the sequence being a child of the previous node. This sequence is sometimes referred to as the *search path* from the root to the node. 
 
 The parent-child relationship defines an ancestor-descendant relationship on nodes in a binary tree. Specifically, a node is an *ancestor* of *d* if it lies on the search path from the root to *d*.  If a node is an ancestor of *d*, we say that *d* is a *descendant* of that node. Our convention is that *d* is an ancestor and a descendant of itself. A node that has no descendants except for itself is called a *leaf*.
 
 The *depth* of a node *n* is the number of nodes on the search path from the root to *n*, not including *n* itself. The *height* of a binary tree is the maximum depth of any node in that tree. A *level* of a tree is all nodes at the same depth. 
 
 A *full binary tree* is a binary tree in which every node other than the leaves has two children. A *perfect binary tree* is a full binary tree in which all leaves are at the same depth, and in which every parent has two children. A *complete binary tree* is a binary tree in which every level, except possibly the last, is completely filled, and all nodes are as far left as possible. This terminology is not universal, e.g, some authors use complete binary tree where we write perfect binary tree. It is straightforward to prove using induction that the number of non-leaf nodes in a full binary tree is one less that the number of leaves. A perfect binary tree of height *h*  contains exactly 2^(h+1) -1 nodes, of which 2^h are leaves. A complete binary tree on n nodes has height floor(log(n)). A left-skewed tree is a tree in which no node has a right child. A right-skewed tree is a tree in which no node has a left child. In either case, we refer to the tree as being skewed.
 
 A key computation on a binary tree is  *traversing* all the nodes in the tree. Traversing is sometimes called *walking*. Here are some ways in which this visit can be done.
 - Traverse the left subtree, visit the root, then traverse the right subtree: an **in-order** traversal.
 - Visit the root, traverse the left subtree, then traverse the right subtree: a **pre-order** traversal.
 - Traverse the left subtree, traverse the right subtree, then visit the root: a **post-order** traversal.


Let *T* be a binary tree of *n* nodes, with height *h*. Implemented recursively, these traversals have O(n) time complexity and O(h) additional space complexity. The space complexity is dictated by the maximum depth of the function call stack. If each node has a parent field, the traversals can be done with O(1) additional space complexity.


- **Recursive algorithms** are well-suited to problems on trees. Remember to include space implicitly allocated on the function call stack when doing space complexity analysis.
- Some tree problems have simple brute-force solutions that use O(n) space solution, but subtler solutions that uses the **existing tree nodes** to reduce space complexity to O(1). 
- Consider **left- and right-skewed trees** when doing complexity analysis. Note that O(h) complexity, where h is the tree height, translates into O(log n) complexity for balanced trees, but O(n) complexity for skewed trees.
- If each node has a **parent field**, use it to make your code simpler, and to reduce time and space complexity.
- It's easy to make the mistake of treating a node that has a single child as a leaf.
 
 