## 1. 代码格式问题：
#### 这个文件 weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,7 +1,8 @@
 # -*- coding: utf-8 -*-
 
+
 def queryFun(cityInput):
-    global hisWeather # 在本函数里更新所查过的城市记录
+    global hisWeather  # 在本函数里更新所查过的城市记录
     dictWeather = {}
 
     with open('..\\resource\\weather_info.txt', 'r', encoding='utf-8') as f:
@@ -17,12 +18,13 @@
         hisWeather.append(cityInput)
         hisWeather.append(weather)
 
+
 def hisFun():
-    for i in range(len(hisWeather)//2):
-        print(hisWeather[i*2] + " " + hisWeather[i*2+1])
+    for i in range(len(hisWeather) // 2):
+        print(hisWeather[i * 2] + " " + hisWeather[i * 2 + 1])
 
 
-hisWeather = [] # 定义一个全局变量存放所有查询过的城市的天气情况
+hisWeather = []  # 定义一个全局变量存放所有查询过的城市的天气情况
 
 while True:
 
@@ -44,4 +46,3 @@
 
     else:
         queryFun(cmdInput)
-        
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 weather.py 的 3-18 行
函数 `queryFun` Cyclomatic complexity(循环复杂度、条件复杂度)为 (7)，过高、建议缩减
