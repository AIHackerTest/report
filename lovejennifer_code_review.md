## 1. 代码格式问题：
#### 这个文件 imitation.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,24 +1,23 @@
 def daily():
-	print(open('my.log').read())
-	while 1:
-	    d = input(">>> ")
-	    #print(d)
-	    if d in ['q','quit','exit']:
-	    	break
-	    elif d in ['s','sync']:
-	    	#print('sdsdsdsd sds s ...')
-	    	print(open('my.log').read())
-	    elif d in ['?','h','H','help']:
-	    	print('''usage:
+    print(open('my.log').read())
+    while 1:
+        d = input(">>> ")
+        #print(d)
+        if d in ['q', 'quit', 'exit']:
+            break
+        elif d in ['s', 'sync']:
+            #print('sdsdsdsd sds s ...')
+            print(open('my.log').read())
+        elif d in ['?', 'h', 'H', 'help']:
+            print('''usage:
 	    	?|h|H|help help
 	    	s|sync re-load all history msg
 	    	q|quit|exit quit
 	    	''')
-	    else:
-	    	print('saving', d)
-	    	open('my.log', 'a').write('\n'+d)
-
+        else:
+            print('saving', d)
+            open('my.log', 'a').write('\n' + d)
 
 
 if __name__ == '__main__':
-	daily()
+    daily()
```

</details>

#### 这个文件 new_weather.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,50 +1,53 @@
 def load_data(file):
-	dic = {}
-	with open(file) as f:
-		try:
-			document = f.readlines()
-			#print(document)
-			for line in document:
-				info = line.split(',')
-				dic[info[0]] = info[1]
-		except IOError as ioerr:
-			print('%s文件不存在' %(file))
-		return dic
+    dic = {}
+    with open(file) as f:
+        try:
+            document = f.readlines()
+            #print(document)
+            for line in document:
+                info = line.split(',')
+                dic[info[0]] = info[1]
+        except IOError as ioerr:
+            print('%s文件不存在' % (file))
+        return dic
+
 
 def words():
-	 print('''
+    print('''
 	      输入城市名，返回该城市的天气数据；
               输入指令，打印帮助文档（一般使用 h 或 help）；
               输入指令，退出程序的交互（一般使用 quit 或 exit）；
               在退出程序之前，会打印查询过的所有城市.
           ''')
 
+
 def history(l):
-	for i in range(len(l)):
-		print(l[i][0], l[i][1])
+    for i in range(len(l)):
+        print(l[i][0], l[i][1])
+
 
 def search():
-	h = []
-	while True:
-		city = input("输入指令或城市名: ")
-		d = load_data("../resource/weather_info.txt")
-		if city in d.keys():
-			weather = d[city]
-			if [city, weather] not in h:
-				h.append([city, weather])
-			print('{}, {}'.format(city, weather))
-		elif city in ['help','h']:
-			words()
-		elif city == 'history':
-			history(h)
-		elif city in ['exit','quit']:
-			print('推出前输入历史记录: ')
-			history(h)
-			break
-		else:
-			print("请输入正确指令或城市名，输入help或h进入帮助")
-			continue
+    h = []
+    while True:
+        city = input("输入指令或城市名: ")
+        d = load_data("../resource/weather_info.txt")
+        if city in d.keys():
+            weather = d[city]
+            if [city, weather] not in h:
+                h.append([city, weather])
+            print('{}, {}'.format(city, weather))
+        elif city in ['help', 'h']:
+            words()
+        elif city == 'history':
+            history(h)
+        elif city in ['exit', 'quit']:
+            print('推出前输入历史记录: ')
+            history(h)
+            break
+        else:
+            print("请输入正确指令或城市名，输入help或h进入帮助")
+            continue
+
 
 if __name__ == '__main__':
-	search()
-
+    search()
```

</details>


## 2. 代码相似问题：


## 3. 复杂度及其他问题：
#### 文件 new_weather.py 的 26-46 行
函数 `search` Cyclomatic complexity(循环复杂度、条件复杂度)为 (7)，过高、建议缩减

#### 文件 weather.py 的 12-12 行
Error: invalid syntax (<unknown>, line 12)
