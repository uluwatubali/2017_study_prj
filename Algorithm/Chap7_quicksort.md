
# Quicksort

```
Quicksort(Item a[], int l, int r){
  if(l<=r) return;  
  int i = partition(a, l, r);
  quicksort(a, l, i-1);
  quicksort(a, i+1, r);
}

int partition(Item a[], l, r){
  int i,j;
  Item v = a[r];
  i = l-1;
  j = r;
  for(;;){
    while(a[++i]<v);
    while(a[--j]>v)if(j==i)break;
    if(l<=r) break;
    exch(a, i, j);
  }
  exch(a, i, r);
  return i;
}
```
