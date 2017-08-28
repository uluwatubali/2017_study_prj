# Mergesort
Idea: Merge 2 ordered list, A[] and B[] to C[]
1. Top-down:divide-and-conquer
2. Bottom-up: combined and 
3. Time = Nln(N)
4. Sequential access: it would be efficient on some architecture
5. Insensitive to input (Quicksort is slow with ordered list)

6. Need extra space or using in-place merge sort

Prove of O(nlgn):
  > **T(n) = C + 2T(n/2) + Cn**
  > After drawing the tree, we can see the level of tree is (1+lgn). Each level has cn steps in total.
  > Hence, total operations is cn*(1+lgn)= O(nlgn)

```
void mergeAB(Item A[], Item B[], Item c[], M, N){
  for(int i=j=k=0; k< M+N; k++){    
    if(i == M){C[k]=B[j++];continue;}
    if(j == N){C[k]=A[i++];continue;}
    C[k] = A[i]<B[j]?A[i++]:B[j++];
  }
}

```
