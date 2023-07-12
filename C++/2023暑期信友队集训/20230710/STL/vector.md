# 声明vector

```
vector\<type> name[lenght];
```

# 迭代器

```
vector<type>::iterator name
```

# vector使用

```
#include <iostream>  
#include <vector>  
#include <array>  
using namespace std;  
  
int main(){  
vector<int> v{1,0,1,1,0};//声明一个int类型的vector  
for (vector<int>::iterator it= v.begin()+3; it < v.end()-1 ; it++) {//输出v中的所有元素  
cout << *it << " ";  
}  
for (auto it= v.begin()+3; it < v.end()-1 ; it++) {//输出v中的所有元素  
cout << *it << " ";  
}  
for (auto it:v) {//it为int类型，输出全部v  
cout << it << " ";  
}  
v.push_back(2);//在结尾插入“2” {1,0,1,1,0,2}  
v.pop_back();//删去结尾“2” {1,0,1,1,0}  
  
/*插入*/  
std::vector<int> demo{1,2};  
//第一种格式用法  
demo.insert(demo.begin() + 1, 3);//{1,3,2}  
//第二种格式用法  
demo.insert(demo.end(), 2, 5);//{1,3,2,5,5}  
//第三种格式用法  
std::array<int,3>test{ 7,8,9 };  
demo.insert(demo.end(), test.begin(), test.end());//{1,3,2,5,5,7,8,9}  
//第四种格式用法  
demo.insert(demo.end(), { 10,11 });//{1,3,2,5,5,7,8,9,10,11}  
for (int i = 0; i < demo.size(); i++) {  
cout << demo[i] << " ";  
}  
  
/*删除*/  
auto iter = demo.erase(demo.begin() + 1);//删除元素 2//输出 dmeo 容器新的size  
cout << "size is :" << demo.size() << endl;  
//输出 demo 容器新的容量  
cout << "capacity is :" << demo.capacity() << endl;  
for (int i = 0; i < demo.size(); i++) {  
cout << demo[i] << " ";  
}  
//iter迭代器指向元素 3cout << endl << *iter << endl;  
return 0;  
}
```

# 缺点

1. 耗时
2. RE