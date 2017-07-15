1. Splay Tree
Cached tree: Keep nodes we encountered on the path closer to the root.

2. 2-3-4 Tree
Keep tree balanced and it's easy to understand.But hard to implement

3. Red-Black Tree(RB Tree)
Best one of BST.
worst = 2lgN
avg = 1.002N

Easy to Implement: Lean Left RB(LLRB) Tree
```
Node InsertLLRB(Node h, Key key, int val){
  if(h==null){
    return new node(key, RED);
    return h;
  }
  if(cmp(h,key)<0) h->left = InsertLLRB(h->left, key, val);
  if(cmp(h,key)>0) h->right = InsertLLRB(h->right, key, val);
  if(cmp(h,key) == 0) h->val = val;

  if( isRed(h->right) && !isRed(h->left)) RotL(h);
  if( isRed(h->left) && isRed(h->left->left)) RotR(h);
  if( isRed(h->left) && isRed(h->right)){
    h->left->red = 0;
    h->right->red = 0;
    h->red = 1;
  }

  return h;
}
```
