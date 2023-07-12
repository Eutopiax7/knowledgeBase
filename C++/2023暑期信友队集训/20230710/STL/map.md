# 声明  
  
`map<key,value> mp` `key`为键的类型，`value`是值的类型
  
```  
map<string,int> mp;  
```  
  
# 特点  
  
1. 以键从大到小排序
2. 不会存在相同的键的元素
  
# 访问  
  
```  
map<string,int> mp;  
mp["abc"]+=1;  
mp["bcd"]+=1;  
mp["abc"]+=1;  
cout<<mp["abc"]<<" "<<mp["bcd"];//2 1  
```  
  
## 迭代器访问  
  
```  
for(auto it=mp.begin();it!=mp.end();it++){  
cout<<endl<<it->first<<" "<<it->second;  
}  
```  
  
```  
for(auto it:mp){  
cout<<endl<<it.first<<" "<<it.second;  
}  
```  
  
# 查找  
  
注意：
```  
map<int,int> mp;  
mp[12]+=1;  
mp[25]+=1;  
cout<<mp.size()<<endl;//2  
cout<<mp.count[7]<<endl;  
cout<<mp.size()<<endl;//3  
```