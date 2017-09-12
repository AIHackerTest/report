## 1. 代码格式问题：
#### 这个文件 weather_demo.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,6 +1,6 @@
 def read_file(path):
     try:
-        with open(path, 'r', encoding = 'utf-8') as f:
+        with open(path, 'r', encoding='utf-8') as f:
             content = f.readlines()
             weather_info = {}
     except:
@@ -10,6 +10,7 @@
             line = line.strip('\n').split(',')
             weather_info[line[0]] = line[1].strip("''")
         return weather_info
+
 
 def main():
     path = '../resource/weather_info.txt'
@@ -21,10 +22,10 @@
             weather = weather_info[order]
             history = '%s : %s\n' % (order, weather)
             histories += history
-            print("%s的天气状况为：%s " % (order,weather))
+            print("%s的天气状况为：%s " % (order, weather))
 
         elif order == 'help':
-                print("""
+            print("""
 - 输入城市名，查询该城市的天气；
 - 输入help，获取帮助文档；
 - 输入history，获取查询历史；
@@ -33,11 +34,12 @@
         elif order == 'history' and len(histories) > 0:
             print(histories)
         elif order == 'history' and histories == '':
-                print("暂无记录")
+            print("暂无记录")
         elif order == 'quit':
             return
         else:
             print("查询不到相关城市")
 
+
 if __name__ == "__main__":
-     main()
+    main()
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 weather_demo.py 的 14-40 行
函数 `main` Cyclomatic complexity(循环复杂度、条件复杂度)为 (9)，过高、建议缩减

#### 文件 weather_demo.py 的 1-12 行
函数 `read_file` Cyclomatic complexity(循环复杂度、条件复杂度)为 (6)，过高、建议缩减
