if item is in list:
```
$var in $list
```

What's diferrence between == and is?
 ==: Comparison of content
 is: Comparison of object
```
list1=['abcd']
list2=['abcd']

>> list1 == list2
True
>> list1 is list 2
False

```

Usage of none.
While variable is not 0 nor null and we need to use it without error reference.
```
max_num = none

if(max_num == none):
  max_num = num
else(max_num < next_num):
  max_num = next_num

```

Dictionary, key-value map = Hash map
Key must be constant object, value, string or tuple
To get key-value:
1. dict.get(key): Can use return value 'none' to verify if key is exist or not.
2. dict.get(key, val): if key is not in dict, return val
3. dict[key]: Return KeyError if key is not exist.


Priority Queue & Heap: heapq
heappush(heap_list, (tuple)): heap by tuple
```
from heapq import *

heap_list = []
heappush(heap_list, (tuple))
heap_head_tuple = heappop(heap_list)

```

Sorting with Comparator 
```
class CustomCompare(str):
    def __lt__(x,y):
        return x+y>y+x

class Solution(object):
    def largestNumber(self, nums):
        """
        : Given a list of non negative integers, arrange them such that they form the largest number.
        """
        nums = [str(x) for x in nums]
        nums = sorted(nums,key=CustomCompare)
        return ''.join(nums).lstrip('0') or '0'
```
