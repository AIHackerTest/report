## 1. 代码格式问题：
#### 这个文件 weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -3,9 +3,9 @@
 def load_dict_from_file(filepath):
     dict = {}
     try:
-        with open(filepath,'r') as dict_file:
+        with open(filepath, 'r') as dict_file:
             for line in dict_file:
-                (key,value) = line.strip().split(',') 
+                (key, value) = line.strip().split(',')
                 dict[key] = value
 
     except IOError as ioerr:
@@ -22,9 +22,9 @@
         d = load_dict_from_file('weather_info.txt')
         if city in d.keys():
             weather = d[city]
-            history = '%s : %s\n' % (city, weather) 
+            history = '%s : %s\n' % (city, weather)
             histories = histories + history
-            print("%s的天气情况为： %s" % (city,weather))
+            print("%s的天气情况为： %s" % (city, weather))
         # 这是help
         if city == 'help':
             print("    - 输入城市名，查看相应天气情况")
@@ -38,7 +38,5 @@
         elif city == 'history':
             print(histories)
 
+
 query()
-
-
-
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 weather.py 的 18-39 行
函数 `query` Cyclomatic complexity(循环复杂度、条件复杂度)为 (6)，过高、建议缩减
