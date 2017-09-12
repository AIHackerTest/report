## 1. 代码格式问题：
#### 这个文件 MVP.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,33 +1,31 @@
 d = {}
 h = {}
 #file = open("weather_info.txt")
-with open ("C:/Users/ZHANG/weather_info.txt", 'r' , encoding = 'utf-8') as f:
+with open("C:/Users/ZHANG/weather_info.txt", 'r', encoding='utf-8') as f:
     for info in f.readlines():
         key = info.split(',')[0]
-        d[key]=info.split(',')[1].strip('\n')
+        d[key] = info.split(',')[1].strip('\n')
     #print(d)
-#city = input("please enter the city name:")
-#print ()
+    #city = input("please enter the city name:")
+    #print ()
 while True:
     order = input("请输入指令或您要查询的城市：")
     if order in d.keys():
         h[order] = d[order]
-        print("%s的天气为：%s" %(order, d[order]))
-    elif order == "help" or  order == "h" :
-        print(
-        """
+        print("%s的天气为：%s" % (order, d[order]))
+    elif order == "help" or order == "h":
+        print("""
         输入城市名，查询该城市的天气；
         输入help，获取帮助文档；
         输入history，获取查询历史；
         输入quit 或 exit，退出天气查询系统；
-        """
-        )
+        """)
     elif order == "history":
         for x in h.keys():
-            print (x, h[x])
+            print(x, h[x])
     elif order == "exit" or order == "quit":
         for x in h.keys():
-            print (x, h[x])
+            print(x, h[x])
         break
     else:
-        print ("没有该城市天气信息")
+        print("没有该城市天气信息")
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：