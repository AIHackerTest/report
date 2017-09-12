## 1. 代码格式问题：
#### 这个文件 weatherInquiry.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -2,7 +2,9 @@
 history_weather = {}
 weather_info = {}
 
-def getWeather(file_path = "E:\\161208\\Py101-004\\Chap1\\resource\\weather_info.txt"):
+
+def getWeather(
+        file_path="E:\\161208\\Py101-004\\Chap1\\resource\\weather_info.txt"):
     data = {}
     try:
         with open(file_path, 'r', encoding='utf-8') as f:
@@ -16,14 +18,13 @@
 
 
 def printHelp():
-    print(
-    '''
+    print('''
     输入城市名，返回该城市的天气数据；
     输入h或help，打印帮助文档；
     输入history，打印查询历史；
     输入quit，退出程序。
-    '''
-    )
+    ''')
+
 
 def inquiryWeather(city):
     try:
@@ -36,9 +37,11 @@
         history_weather.update({city: weather})
         return {city: weather}
 
+
 def printHistory():
     for city in history_weather:
         print(city + "\t" + history_weather[city])
+
 
 def checkCommand():
     command = input("请输入指令或城市名：")
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 weatherInquiry.py 的 5-15 行
函数 `getWeather` Cyclomatic complexity(循环复杂度、条件复杂度)为 (6)，过高、建议缩减
