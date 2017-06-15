Symbol Table:
search key and get object back.

Key-Index search
- For key values are in small range. Otherweise, using Sequential search.

Sequential search
- Ordered/Un-ordered: Trade-off between insert or search. (Insertion Sort)
- Array/Link-list: Link-list is easy to insert/remove, and being allocated dynamically.

Binary Search
- Using interpolation search as improvement: Not always at exactly middle position.
m = (l+r)/2;
==>
m = (r-l)*(v-a[l].key)/(a[r].key-a[l].key);

Binary Search Tree

struct Node{
  int value;
  struct Node* left, *right;
}
Node.Value()>= Node.left.Value
Node.Value()<= Node.right.Value
