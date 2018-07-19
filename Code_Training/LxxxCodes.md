
#365. Jug problem 
```
Find GCD

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

It can apply to n/2, n/3, n/4...
```
