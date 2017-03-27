# Mergesort
Idea: Merge 2 ordered list, A[] and B[] to C[]
1. Top-down:divide-and-conquer
2. Bottom-up: combined and 
3. Time = Nln(N)
4. Sequential access: it would be efficient on some architecture
5. Insensitive to input (Quicksort is slow with ordered list)


```
void mergeAB(Item A[], Item B[], Item c[], M, N){
  for(int i=j=k=0; k< M+N; k++){    
    if(i == M){C[k]=B[j++];continue;}
    if(j == N){C[k]=A[i++];continue;}
    C[k] = A[i]<B[j]?A[i++]:B[j++];
  }
}

```
