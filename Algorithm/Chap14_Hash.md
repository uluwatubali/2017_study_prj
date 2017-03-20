# Hash

It's time-space trade off.

Constant insert and search.

No effiecient sort or select

Hash function usually falls in inner loop and dominates running time.

Error usually comes from type converting.

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
