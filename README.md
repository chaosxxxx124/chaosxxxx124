2021.7.4

leetcode第一天，做了几道简单题，没啥说的
检查是否有重复元素：
if len(a)==len(set(a))

2021.7.5
第二天，主要收获是列表和整数、字符串的转换：
lst = list(map(int,str(number)))
number = "".join(map(list(str,lst)))
两个列表的差集
lst_diff = list(set(lst1)^set(lst2))
跟出现次数有关的题：hashtable

2021.7.6
第三天
collections.Counter计数器
正常情况下自己写计数器是这样写                                         collections.Counter的写法：
colors = ['red', 'blue', 'red', 'green', 'blue', 'blue'                 from collections import Counter                                  
result = {}                                                             colors = ['red', 'blue', 'red', 'green', 'blue', 'blue']
for color in colors:                                                    c = Counter(colors)     
    if result.get(color)==None:                                         print (dict(c))
        result[color]=1                                                 #{'red': 2, 'blue': 3, 'green': 1}
    else:
        result[color]+=1
print (result)
#{'red': 2, 'blue': 3, 'green': 1}

enumerate()：将字典的key和value放一起返回成列表：[(key1,value1)(key2,value2)...]


将一个字符串只保留字母和数字，且全部转为小写放进列表敌我答案对比：（麻烦的是我的）
# s_list = list(s.lower())
        # for i in range(len(s_list)-1,-1,-1):
        #     # print(s_list[i])
        #     if s_list[i].isalpha() or s_list[i].isdigit():
        #         pass
        #     else:
        #         s_list.remove(s_list[i])
        
s_list = "".join(ch.lower() for ch in s if ch.isalnum())
join(要放进目标列表的元素 for 元素 in 字符串 if 筛选条件)
