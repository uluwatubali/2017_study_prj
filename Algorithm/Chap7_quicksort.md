
# Quicksort
Worst Cases: N^2/2  
Average Case: 2N * ln(N)
Best Cases: N*lg(N) A 

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

## Stack Size Control
Using Nonrecursive quicksort and sort smaller subfile first.
Stack never has more than lg(N) entries

## Improvement
Using Insertion sort for small subfiles
- M in range from 5~25 can get 10% improvement

Try to get balance partition by using Median-of-Three Partition
- Choose 3 element and sort into a[Smallest], a[Median], a[Largest], then using a[Median] as partitioning element
- p.333

Improve on duplicate keys by tree-way partition
- Put elements equal to the partitioning element in position of middle part and exclude them from subfiles for recursive calls.
- p.338

String and Vectores: Using tree-way partition

## Select k-th item by quicksort
Comparision: (2+2ln2)*N  
Steps: O (log N)
