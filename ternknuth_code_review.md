## 1. 代码格式问题：
#### 这个文件 ch1.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,17 +1,18 @@
 #!/usr/bin/env python3
+
 
 def print_help():
     ''' 打印帮助文档
 
     '''
-    help_message = ["输入城市名，返回该城市的天气数据；",
-                    "输入指令 h 或 help ，打印帮助文档；",
-                    "输入指令 q 、quit 或 e 、exit ，退出程序的交互；",
-                    "在退出程序之前，打印查询过的所有城市。"]
+    help_message = [
+        "输入城市名，返回该城市的天气数据；", "输入指令 h 或 help ，打印帮助文档；",
+        "输入指令 q 、quit 或 e 、exit ，退出程序的交互；", "在退出程序之前，打印查询过的所有城市。"
+    ]
     for i in help_message:
         print("\t{0}".format(i))
 
-        
+
 def print_history_record(list_history_record):
     ''' 打印查询历史记录
 
@@ -19,13 +20,13 @@
     if list_history_record:
         print("\t------查询历史记录------")
         for i in list_history_record:
-            print("\t{0[0]} {0[1]}".format(i) )
+            print("\t{0[0]} {0[1]}".format(i))
         else:
             pass
     else:
         print("\t尚未查询过城市天气！")
-        
-        
+
+
 def get_city_weather(city_name, dict_weather_data):
     ''' 查询城市天气
 
@@ -59,12 +60,14 @@
     ''' 主程序
 
     '''
-    list_command = {'h' : 'help',
-                    'help' : 'help',
-                    'q' : 'quit',
-                    'quit' : 'quit',
-                    'e' : 'quit',
-                    'exit' : 'quit'}
+    list_command = {
+        'h': 'help',
+        'help': 'help',
+        'q': 'quit',
+        'quit': 'quit',
+        'e': 'quit',
+        'exit': 'quit'
+    }
     list_history_record = []
     file = '../resource/weather_info.txt'
     weather_data = make_weather_data(file)
@@ -80,11 +83,11 @@
             else:
                 pass
         elif input_value in weather_data:
-            result = (input_value, get_city_weather(input_value, weather_data) )
-            print("\t{0[0]} {0[1]}".format(result) )
+            result = (input_value, get_city_weather(input_value, weather_data))
+            print("\t{0[0]} {0[1]}".format(result))
             list_history_record.append(result)
         else:
-            print( "\t该指令或城市名不存在，请重新输入！ （需要帮助请输入‘h’戓‘help’）" )
+            print("\t该指令或城市名不存在，请重新输入！ （需要帮助请输入‘h’戓‘help’）")
             continue
 
 
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 ch1.py 的 58-88 行
函数 `main` Cyclomatic complexity(循环复杂度、条件复杂度)为 (6)，过高、建议缩减
