
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
int BS_It(vector<int> &nums, int l, int r, int key){
  while(l<=r){
    int m = (l+r)/2;
    if( nums[m] == key) return m;
    
    if(nums[m]>key)
      r = m-1;
    else
      l = m+1;
  }

}
```
If not found, compare key to nums[l] or nums[r] (l and r will be the same) to see key should be located between which 2 indexes. 
