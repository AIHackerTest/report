## 1. 代码格式问题：
#### 这个文件 weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -2,7 +2,10 @@
 # -*- coding: utf-8 -*-
 
 #以utf-8的编码模式打开txt文件
-with open('/Users/zjiaqiao/Py101-004/Chap1/resource/weather_info.txt','r', encoding = 'utf-8') as f:
+with open(
+        '/Users/zjiaqiao/Py101-004/Chap1/resource/weather_info.txt',
+        'r',
+        encoding='utf-8') as f:
     data = f.readlines()
 
 dict = {}
@@ -10,14 +13,14 @@
 for line in data:
     dict[line.strip().split(',')[0]] = line.strip().split(',')[1]
 
-history ={}
+history = {}
 
 while True:
     print('请输入指令或您要查询的城市名')
     city = input('>')
 
     if city in dict.keys():
-        print('%s的天气状况为: %s' % (city,dict[city]))
+        print('%s的天气状况为: %s' % (city, dict[city]))
         history[city] = dict[city]
     elif city == 'help':
         print("""
@@ -32,4 +35,4 @@
         print("历史查询记录:%s" % history)
         exit(0)
     else:
-        print("抱歉，无法查询到%s的天气状况。" % city )
+        print("抱歉，无法查询到%s的天气状况。" % city)
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：