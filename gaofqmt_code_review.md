## 1. 代码格式问题：
#### 这个文件 weather_query.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -5,7 +5,7 @@
 
 from sys import exit
 with open('../resource/weather_info.txt', 'r') as file:
-   weather =  [x.rstrip('\n') for x in file.readlines()]
+    weather = [x.rstrip('\n') for x in file.readlines()]
 
 weather_d = []
 history = {}
@@ -21,7 +21,7 @@
     city = input("请输入指令或要查询的城市名称> ").strip()
 
     if city == 'help':
-        print ("""
+        print("""
         输入城市名，查询天气状况;
         输入help，获取帮助;
         输入history，获取查询历史;
@@ -29,11 +29,11 @@
         """)
     elif city == "history":
         for x, y in history.items():
-            print (x, y)
+            print(x, y)
     elif city == 'quit':
         file.close()
         exit(1)
-    elif not(city in weather_d.keys()):
+    elif not (city in weather_d.keys()):
         print("您输入的城市暂未收录，请重新输入！")
         continue
     else:
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：