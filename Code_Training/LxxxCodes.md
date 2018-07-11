
#365. Jug problem 
Find GCD

```
int findGCD(int x, int y){
        while( y != 0){
            int temp = y;
            y = x % y;
            x = temp;
        }
    return x;
}
```
