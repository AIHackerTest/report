## 1. 代码格式问题：
#### 这个文件 query_weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -11,7 +11,10 @@
 weather_info = {}
 history = {}
 
-with open('d:\PythonTools\ZY.Py101-004\Chap1\project\weather_info.txt', 'r',encoding='utf-8_sig') as f:
+with open(
+        'd:\PythonTools\ZY.Py101-004\Chap1\project\weather_info.txt',
+        'r',
+        encoding='utf-8_sig') as f:
     weather_tbl = f.readlines()
 
 for line in weather_tbl:
@@ -30,7 +33,7 @@
 
     elif cityinput == 'history':
         for histcity in history:
-            print(histcity, history[histcity],end='')
+            print(histcity, history[histcity], end='')
 
     elif cityinput in ['h', 'help']:
         print('''
@@ -43,7 +46,7 @@
     elif cityinput in ['quit', 'q']:
         print("历史查询记录：")
         for histcity in history:
-            print(histcity, history[histcity],end='')
+            print(histcity, history[histcity], end='')
         break
 
     else:
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：