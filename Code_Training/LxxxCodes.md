
#365. Jug problem 
```
Two jugs with size x and y. Estamation size of jug z.

Let d = GCD(x,y), then there's alway nonzero integers a and b, such that ax + by = d. Bézout's identity (also called Bézout's lemma)
If z is multiple of GCD(x,y), then the answer is yes.


int findGCD(int x, int y){
        while( y != 0){
            int temp = y;
            y = x % y;
            x = temp;
        }
    return x;
}
```

368. Largest Divisible Subset
```
dp[n] = dp[0~n-1]+1;
ex:
nums = [1,2,30,50,60]
dp[4] = max{dp[2] + 1, dp[1] + 1, dp[0]+1};


for(i:0 to n){
        for(j:0 to i-1){
                if(T[i]<T[j]+1 && nums[i]%nums[j] ==0)
                        T[i] =  T[j]+1;
                
        }
}
```

#229. Maj Element II
```
Boyer-Moore Majority Vote algorithm
https://gregable.com/2013/10/majority-vote-algorithm-find-majority.html
Try [3,3,3,4,1,2,0]
It can apply to 2, 3, 4 majority number (n/2, n/3, n/4...)
```

#304. Range Sum Query 2D - Immutable
```
O(nm) space, O(1)Time

Step1. get sum matrix
Step2. caclulate obj sum
+-----+-----+
|  A  |  B  |
+-----+-----+
|  C  |  D  |
+-----+-----+
rect[D] = rect[A+B+C+D] - rect[A+C] - rect[A+B] + rec[A]

```
