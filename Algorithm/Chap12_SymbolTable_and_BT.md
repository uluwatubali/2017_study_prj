# Symbol Table:
search key and get object back.

## Key-Index search
- For key values are in small range. Otherweise, using Sequential search.

## Sequential search
- Ordered/Un-ordered: Trade-off between insert or search. (Insertion Sort)
- Array/Link-list: Link-list is easy to insert/remove, and being allocated dynamically.

## Binary Search
- Using interpolation search as improvement: Not always at exactly middle position.
m = (l+r)/2;
==>
m = (r-l)*(v-a[l].key)/(a[r].key-a[l].key);

## Binary Search Tree

- Efficient select, sort
- search, insert, sort are easy to implement and perform well
- Need extra space for links
- Could possibly be unbalanced and lead to slow perfromance.

- Insert == Search + Add node

struct Node{
  int value;
  struct Node* left, *right;
}
Node.Value()>= Node.left.Value
Node.Value()<= Node.right.Value

- Rotation
Some operations get benefit from rotation:
1. Increase search hit by keeping new node as Root
2. Keep trees from unbalanced
3. Remove, Join

- Selection
Need an extra space for 'count' member. Count = # of nodes of its subtree
Partition: put the k_th smallest node at the root
Partition = Select + Rotate(p536)


- Remove: High cost in tree structure
Lazy way: Marked removed node as unused node. We still have to consider time and space.

Steps of remove node X
1. Search X
2. Combine 2 subtrees of X
2.1 Partition(X->r, 0): put the smallest node Y of right subtree at the root
2.2 Y->left = X->left: After 2.1, Y is root of subtree and has no left link. 
3. delete X

- Join
O(n): Linear 

Steps of Join A and B BST
1. Put root of A, Node_A, into B. And let node_A become root of B
2. Join 2 left(2 right) subtrees of A & B(Root is NodeA now)
Join left subtree of node_A in subtree B and left subtree of Node_A in tree A.
Join right subtree of node_A in subtree B and right subtree of Node_A in tree A.
