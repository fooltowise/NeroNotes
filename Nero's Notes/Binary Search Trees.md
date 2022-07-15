# Binary Search Trees
BST are a workhorse of data structures and can be used to solve almost every data  structures problem reasonably efficiently. They offer the ability to efficiently search for a key as well as find the *min* and *max* elements, look for the successor or predecessor of a search key (which itself need not to be present in the BST), and enumerate the keys in a range in sorted order.

BSTs are similar to arrays in that the stored values (the "keys") are stored in a sorted order. However, unlike with a sorted array, keys can be added and deleted from a BST efficiently. Specifically, a BST is a [[Binary Trees| binary tree]] in which the nodes store keys that are comparable, e.g, integers or strings. The keys stored at nodes have to respect the BST property - the key stored at a node is greater than or equal to the keys stored at the nodes of its left subtree and less than or equal to the keys stored in the nodes of its right subtree.


Key lookup, insertion, and deletion take time proportional to the height of the tree, which can in worst case be O(n), if insertions and deletions are naively implemented. However there are implementations of insert and delete which guarantee that the tree has height O(log n). These require storing and updating additional data at the tree nodes. Red-black trees are an example of height-balanced BSTs and are widely used in data structure libraries.

A common mistake with BSTs is that an object that's present in a BST is not updated. The consequence is that a lookup for that object returns false, even though it's still in the BST. As a rule, avoid putting mutable objects in a BST. Otherwise, when a mutable object that's in a BST is to be updated, always first remove it from the tree, then update it, then add it back.


The BST prototype is as follows:


```java
public class BSTNode<T> extends TreeLike<T, BstNode<T>>{
	public T data;
	public BSTNode<T> left, right;
}
```

### Binary Tree Search boot camp

Searching is the single most fundamental application of BSTs. Unlike a hash table, a BST offers the ability to find the min and max elements, and find the next largest/next smallest element. These operations, along with lookup, delete and find, take time O( log n) for library implementations of BSTs. Both BSTs and hash tables use O(n) space . in practice, a BST uses slightly more space.

The following program demonstrates how to check if a given value is present in a BST. It is a nice illustration of the power of recursion when operating on BSTs.

```java
public static BSTNode<Integer> searchBST(BSTNode<Integer> tree, int key){
	return tree == null || tree.data == key 
	? tree
    : key < tree.data ? searchBST(tree.left, key)
								 : searchBST(tree.right, key);
}

```

Since  the program descends tree with in each step, and spends O(1) time per level, the time complexity is O(h), where h is the height of the tree.

[[Know your binary search tree libraries]]

### Top tips for Binary Search Trees
- With a BST you can **iterate** through elements in **sorted order** in time O(n) regardless of whether it is balanced
- Some problems need a **combination of a BST and a hash table**. For example, if you insert student objects into a BST and entries are ordered by GPA, and then a student's GPA needs to be updated and all we have is the student's name and new GPA, we cannot find the student by name without a full traversal. However, with an additional hash table, we can directly go to the corresponding entry in the tree.
- Sometimes, it is necessary to **augment** a BST to make it possible to manipulate more complicated data, e.g, intervals, and efficiently support more complex queries, e.g. the number of elements in a range.
- The BST property is a **global property** - a binary tree may have the property that each node's  key is greater than the key at its left child and smaller than the key at its right child, but it may not be a BST.










