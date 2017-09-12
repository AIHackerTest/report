## 1. 代码格式问题：
#### 这个文件 ch1_weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -2,7 +2,7 @@
 # 创建字典，打开文件，把文本内容存储到文件
 dic_weather = {}
 dic_history = {}
-f = open('weather_info.txt','r',encoding='utf-8')
+f = open('weather_info.txt', 'r', encoding='utf-8')
 for line in f:
     (city, weather) = line.strip().split(',')
     dic_weather[city] = weather
@@ -13,26 +13,24 @@
     if user_input in dic_weather.keys():
         weather = dic_weather[user_input]
         dic_history[user_input] = weather
-        print ('%s的天气状况为:%s' % (user_input,weather))
+        print('%s的天气状况为:%s' % (user_input, weather))
 
     elif user_input == 'help':
-        print(
-        """
+        print("""
             输入城市名，查询该城市的天气；
             输入 help, 获取帮助文档；
             输入 history, 获取查询历史；
             输入 quit, 退出天气查询系统.
-        """
-        )
+        """)
 
     elif user_input == 'history':
         for user_input in dic_history:
-            print (user_input,dic_history[user_input])
+            print(user_input, dic_history[user_input])
         else:
-            print ('您尚未查询。')
+            print('您尚未查询。')
 
     elif user_input == 'quit':
         break
     else:
-        print ("您输入的指令不存在，请重新输入。")
-f.close()+        print("您输入的指令不存在，请重新输入。")
+f.close()
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：