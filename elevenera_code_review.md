## 1. 代码格式问题：
#### 这个文件 weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,9 +1,9 @@
 import sys
 dic = {}
 
-with open('weather_info.txt','r', encoding='utf-8') as f:
+with open('weather_info.txt', 'r', encoding='utf-8') as f:
     for line in f.readlines():
-        key, value =line.strip().split(',')
+        key, value = line.strip().split(',')
         dic[key] = value
 
 history = []
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：