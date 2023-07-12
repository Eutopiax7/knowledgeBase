# 与set的关系

multiset不去重，set去重  

# 删除某个值

```
multimap<int> s{1,0,0,8,6};  
s.eraser(0);//删除所有0
```

```
multimap<int> s2{1,0,0,8,6};  
s2.eraser(s2.find(0));//删除一个0
```