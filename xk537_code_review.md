## 1. 代码格式问题：
#### 这个文件 ch1.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,7 +1,8 @@
 #coding:utf-8
 
 # 读取天气文件中的数据
-with open('/Users/mic/py101-004/Chap1/resource/weather_info.txt','r') as weather_file:
+with open('/Users/mic/py101-004/Chap1/resource/weather_info.txt',
+          'r') as weather_file:
     weather_data = weather_file.readlines()
     # print (weather_data)测试数据是否成功读取文本数据
 
@@ -16,22 +17,25 @@
 
 history_query = {}
 while True:
-    user_input = input ("请输入您要查询的城市名称：")
+    user_input = input("请输入您要查询的城市名称：")
     if user_input == 'quit' or user_input == 'q':
         exit(0)
 
     elif user_input == 'help':
-        print ("请输入城市名称，查询该城市的天气;\n输入help，获取帮助文档；\n输入history,获取查询历史；\n输入quit 或者 q 退出程序\n")
+        print(
+            "请输入城市名称，查询该城市的天气;\n输入help，获取帮助文档；\n输入history,获取查询历史；\n输入quit 或者 q 退出程序\n"
+        )
 
     elif user_input in city_weather.keys():
-        print ("{0}的天气是：{1}".format(user_input, city_weather[user_input]))
+        print("{0}的天气是：{1}".format(user_input, city_weather[user_input]))
         # 历史查询记录
         history_query_key = user_input
         history_query[history_query_key] = city_weather[user_input]
 
     elif user_input == 'history':
         for history_query_key in history_query:
-            print ("{0}: {1}".format(history_query_key,history_query[history_query_key]))
+            print("{0}: {1}".format(history_query_key, history_query[
+                history_query_key]))
 
     else:
-        print ("输入有误，请输入正确的城市名称或者help")
+        print("输入有误，请输入正确的城市名称或者help")
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：