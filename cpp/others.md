1.sort

acsending sort

```
vector<int> data;
sort(data.begin(), data.end());

or

sort(data.begin(), data.end(), [](int a, int b){return a < b;});

```
Define sort rule

```
vector<myStruct> data;

sort(data.begin(), data.end(), [] (struct myStruct a, struct myStruct b){ return a.value < b.value;});
or
sort(data.begin(), data.end(), [] (const struct myStruct& a, const struct myStruct& b){ return a.value < b.value;});
```

2. quick struct/class init

```
struct myStruct{
  int index;
  int value;
  myStruct(int i, int v):index(i), value(v){}
}
```
