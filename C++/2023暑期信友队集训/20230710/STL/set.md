# 特点  
  
1. 去重
2. 排序
3. 快速查找、删除
  
# 声明  
  
# 函数  
  
## 函数  
  
`insert(key_value)`插入某个值
`insert(first,end)`将定位器first到second之间的元素插入到set中，返回值是void
`find(x)`返回迭代器
`eraser(first,last)`删除，前闭后开
`clear`清空set
  
## 查询函数  
  
`lower_bound(x)`大于等于x
`upper_bound(x)`大于x
`size()`set中元素的个数
`emepty`空为1，非空为0
`count(x)`计算set中x的个数，由于set自动去重，所以返回值只能为1或0，用于查看set中有无x