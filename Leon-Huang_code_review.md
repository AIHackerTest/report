## 1. 代码格式问题：
#### 这个文件 test.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -2,7 +2,6 @@
 
 file = '../resource/15.txt'
 weather_dict = {}
-
 '''
 with open(file) as f:
     data = f.readlines()        # data --> List
@@ -42,4 +41,4 @@
         weather_dict[info[0]] = info[1]
 
 print(weather_dict)
-'''+'''
```

</details>

#### 这个文件 weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,4 +1,5 @@
 # coding: utf-8
+
 
 def generate_dict(file):
     weather_dict = {}
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 weather.py 的 44-73 行
函数 `main` Cyclomatic complexity(循环复杂度、条件复杂度)为 (7)，过高、建议缩减
