
### Selection Sort

Select 1st-smallest, and put to 1st position.
Select 2nd-smallest, and put to 2nd position.
...etc

Worst: N^2/2  
Average: N^2/2  
Good at: Least overhead of exchanging item    
Insensitive to input  

### Insertion Sort  

Like insert new card into your sorted cards.

Optimization: Sentinel Key p.276  
Best:N  
Average:N^2/4  
Worst:N^2/2  
Good at: Partial ordered.(Sensitive to input)
Complexity comes from cmp and swap
Improve comparison by using binary search.

### Bouble Sort  

Compare & exchange from the bottom to up, like bouble pops up.

Optimization: Testing if No exchanges in one pass.  
Best: N-1  
Avg=worst: N^2/2  

### Shell Sort  
Best Increment: Inc(i)=3*Inc(i-1)+1  
or: Inc(i) = 4^(i+1) + 3*2^i +1  
worst: Inc(i)=2^i  

### Abstract Data Type for sort  
Array Interface, Implementation: Output, Input  
Item Interface, Implementation: Comare, operator overload, Outpu, Input  


### Indext, Pointer Sorting  
Indirect to item  
no need to exchange items. If we need to exchange, we use In-Place sort  
Typical example: qsort()  

