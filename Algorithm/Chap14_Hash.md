# Hash

* Time-space trade off.
* Good at insert, search, remove.
* Not for sort, select
* Hash function usually falls in inner loop and dominates running time.
* Error usually comes from type converting.

## Hash Function

Chance of collision should be as close to 1/M as total radomiztion with table size M

Hash function for number
```
// #1, key is floating point in the range from s to t
int hash(key v, int M){
    return (int) M*(v-s)/(s-t);
}

// #2, key is integer in the range from s to t
int hash(key v, int M){
    return v%M;
}
// #3, M is not prime
int hash(key v, int M){
    return (int) (0.616161*(float) v) % M;
}
// #4, M is not prime, key is integer
int hash(key v, int M){
    return (int) (1.616161*(unsigned) v) % M;
}
```
Hash function for strings
```
// #1 
int hash(char *v, int M){
    int a = 127; h=0;
    for(; *v!=0; v++){
        h = (a*h + *v) % M;
    }
    return h;
}

// #2 Universal Hash function
int hash(char* v, int M){
    int a = 31415, b = 27183;
    for(; *v ! = 0; v++, a= a*b % (M-1))
    {
        h = (a*h + *v) % M;
    }
    return h < 0 ? (h + M): h;
}

```

Choose hash table size to be Prime for modular hashing
We can look up a prime number from table or Mersenne primes.

# Seperate Chaining
Hash table with size M and N items and using seperated lists
1. Probablity of each list with item# < N/M is close to 1
2. Birthday Problem: Insert X items before getting collision. X = (pi * M/2)^1/2 = 1.25 M^(1/2)
3. Coupon Collector Problem: Inser X items before each list has at least 1 item. X = MH(M)

Usually use unordered-list
1. Quick insert and easy implementation
2. Stack behavior for easily removing most recently inserted

Provide sorted items by having ordered-list and merge list with N * lg(M)

# Linear Probing
- Total Items = N, Table size = M, M > N
- When there is Hash collision, search right next position.
- Need extra table size. Save extra links.
- Operation Delete: Need to avoid loophold left by removed one.
  - Solution 1. re-Hash the following items
  - Solution 2. Put nullItem with reused flag
