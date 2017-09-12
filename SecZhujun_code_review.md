## 1. 代码格式问题：
#### 这个文件 weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,17 +1,21 @@
 # -*- coding: utf-8 -*-
 import csv
+
+
 def row_csv2dict(csv):
-    dict_club={}
-    with open('weather_info.txt',"r", encoding = "utf-8") as f:
-        reader=csv.reader(f,delimiter=',')
+    dict_club = {}
+    with open('weather_info.txt', "r", encoding="utf-8") as f:
+        reader = csv.reader(f, delimiter=',')
         for row in reader:
-            dict_club[row[0]]=row[1]
+            dict_club[row[0]] = row[1]
     return dict_club
 
+
 def help():
-	print('输入城市名查询天气')
-	print('输入history查询历史')
-	print('输入quit退出')
+    print('输入城市名查询天气')
+    print('输入history查询历史')
+    print('输入quit退出')
+
 
 def main():
     file = row_csv2dict(csv)
@@ -22,19 +26,19 @@
     while True:
         city = input()
         if city == 'help':
-        	help()
+            help()
         elif city in file:
-        	print(file.get(city))
-        	city = city + ' ' + file.get(city)
-        	history.append(city)
-        	#print(history)
+            print(file.get(city))
+            city = city + ' ' + file.get(city)
+            history.append(city)
+            #print(history)
         elif city == 'history':
-        	for i in history:
-        		print(i)
+            for i in history:
+                print(i)
         elif city == 'quit':
-        	break
+            break
         else:
-        	print('输入有误')
+            print('输入有误')
 
 
 main()
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 weather.py 的 16-37 行
函数 `main` Cyclomatic complexity(循环复杂度、条件复杂度)为 (7)，过高、建议缩减
