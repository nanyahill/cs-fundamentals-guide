Binary Search trees
- Inorder traversal of BST always produces sorted output.
- We can construct a BST with only Preorder or Postorder or Level Order traversal. Note that we can always get inorder traversal by sorting the only given traversal.
- Number of unique BSTs with n distinct keys is Catalan Number
- When inserting a new node to a bst, after insertion, the new node would be a leaf node.
- When deleting a node with two children from a BST, when the node is found its successor must only have one child (i.e. a right child) (Note if it had a left child then that child should be the successor).

Advantages of BST over Hash Table
Hash Table supports following operations in Θ(1) time.
1) Search
2) Insert
3) Delete

The time complexity of above operations in a self-balancing Binary Search Tree (BST) (like Red-Black Tree, AVL Tree, Splay Tree, etc) is O(Logn).
So Hash Table seems to beating BST in all common operations. When should we prefer BST over Hash Tables, what are advantages. Following are some important points in favor of BSTs.

We can get all keys in sorted order by just doing Inorder Traversal of BST. This is not a natural operation in Hash Tables and requires extra efforts.
Doing order statistics, finding closest lower and greater elements, doing range queries are easy to do with BSTs. Like sorting, these operations are not a natural operation with Hash Tables.
BSTs are easy to implement compared to hashing, we can easily implement our own customized BST. To implement Hashing, we generally rely on libraries provided by programming languages.
With Self-Balancing BSTs, all operations are guaranteed to work in O(Logn) time. But with Hashing, Θ(1) is average time and some particular operations may be costly, especially when table resizing happens.

Nanya's thoughts from implementing BST
- Inorder successor is a popular question that is simple iteratively but its recursive solution is tricky.
- Recursive algorithms for BST, have if elses from less, greater than AND equal to.
- LCA is another popular question that is simple and tricky especially for Binary Trees.
