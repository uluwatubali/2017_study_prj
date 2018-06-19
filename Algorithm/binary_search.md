
Recursive:
```
int BS_rec(vector<int> &nums, int l, int r, int key){

  if(l>r) return -1;
  int m = (l+r)/2;
  if( nums[m] == key) return m;
  if(l==r) return -1;    
  if(nums[m]> key) return BS(nums, l, m-1, key);
  else return BS(nums, m+1, l, key);
  
}
```
Iterative:
```
int BS_It(vector<int> &nums, int bound_Left, int bound_Right, int key){
  int l, r;
  l = bound_Left;
  r = bound_Right
  while(l<=r){
    int m = (l+r)/2;
    if( nums[m] == key) return m;
    
    if( nums[m] > key )
      r = m-1;
    else
      l = m+1;
  }
  
  if(l == bound_Left - 1){
    // all the elements are larger than key
  }else if(r == bound_Right + 1){
    // all the elements are less than key
  }else{
    // key is in between r and l
    // r is on left side of l
    // l is on right side of r
  }
  

}
```
If not found, compare key to nums[l] or nums[r] (l and r will be the same) to see key should be located between which 2 indexes. 
