1. QuickSort
```
void quickSort(int A[], int start, int end){
  int left = start;
  int right = end;
  int pivot = A[(start + end) / 2];
  
  while(left <= right){
    while(left <= right && A[left] < pivot)
      left++;
    while(left <= right && A[right] > pivot)
      right--;
     if(left <= right){
      int temp = A[left];
      A[left] = A[right];
      A[right] = temp;
      left++;
      right--;
     }
  }
}
```

2. QuickSelect, find Kth largest/smallest
O(n) = O(n) + O(n/2) + O(n/4) + .... = O(n)
```
int quickSelect(int A[], int start, int end, int k){
  int left = start;
  int right = end;
  int pivot = A[(start + end) / 2];
  while(left <= right){
    while(left <= right && A[left] < pivot)
      left++;
    while(left <= right && A[right] > pivot)
      right--;
     if(left <= right){
      int temp = A[left];
      A[left] = A[right];
      A[right] = temp;
      left++;
      right--;
     }
  }
  if(start + k - 1 <= left)
    return quickSelect(A, start, left, k);
  else
    return quickSelect(A, right, end, k - (left - start));
  else
    return A[right + 1];
}
```
