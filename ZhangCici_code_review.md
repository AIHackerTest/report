## 1. 代码格式问题：
#### 这个文件 ch1-project.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -5,32 +5,30 @@
 city_weather = {}  # 建立两个字典
 history = {}
 
-
-f = open('/Users/zhangxi12/temp/weather_info.txt','r')  #打开文本  
-    
+f = open('/Users/zhangxi12/temp/weather_info.txt', 'r')  #打开文本
 
 for line in f:  #读取文本
-    data = line.strip('\n').split(',')   #按照换行和逗号切割
-    city_weather[data[0]] = data[1]   #将文件文本写入字典
-    
+    data = line.strip('\n').split(',')  #按照换行和逗号切割
+    city_weather[data[0]] = data[1]  #将文件文本写入字典
+
 # 用input()接入输入
 
-while True:   #循环
-    
+while True:  #循环
+
     city = input("请输入您想查询的城市或指令：")  #用input()接收输入
-    if city in city_weather.keys(): #如果输入在字典里的关键词里
-        print("%s明天的天气是：%s"% (city,city_weather[city]))  #使用print打印文本
+    if city in city_weather.keys():  #如果输入在字典里的关键词里
+        print("%s明天的天气是：%s" % (city, city_weather[city]))  #使用print打印文本
         history[city] = city_weather[city]  #把历史记录存入字典
-    
-    elif city =="h":  #返回帮助内容
+
+    elif city == "h":  #返回帮助内容
         print("如果您想知道某城市天气，请输入城市名。")
         print("如果您想知道工具使用说明，请输入 h ")
         print("如果您想显示历史记录并退出程序，请输入 q")
-    
-    elif city =="q": 
-        for city in history: #读取history字典
-            print(city,history[city])
-        break #退出运行
-    
+
+    elif city == "q":
+        for city in history:  #读取history字典
+            print(city, history[city])
+        break  #退出运行
+
     else:
         print("您输入的城市不存在，试试别的？")
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：