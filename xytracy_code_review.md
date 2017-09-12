## 1. 代码格式问题：
#### 这个文件 ch0_homework.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,31 +1,28 @@
 import random
-set_number=random.randint(1,20)
+set_number = random.randint(1, 20)
 #生成1-10间的随机数
-for i in range(0,10):
-    num=input("请输入你猜的数字:\n>")
-    if num.isdigit()==True:
-        if (int(num)<1 or int(num)>20):
+for i in range(0, 10):
+    num = input("请输入你猜的数字:\n>")
+    if num.isdigit() == True:
+        if (int(num) < 1 or int(num) > 20):
             print("请输入1-20间的数字！")
-        elif (int(num)>=1 and int(num)<=20):
+        elif (int(num) >= 1 and int(num) <= 20):
 
-
-            if (int(num) < set_number)  :
+            if (int(num) < set_number):
                 print("你猜的太小了！")
-                print("你已经猜了%d次" %(i+1) )
-            elif( int( num )> set_number):
+                print("你已经猜了%d次" % (i + 1))
+            elif (int(num) > set_number):
                 print("你猜的太大了！")
-                print("你已经猜了%d次" %(i+1) )
+                print("你已经猜了%d次" % (i + 1))
             else:
                 break
-            if (i==9):
-                print("你在 %d 次内没能猜出结果" %(i+1) )
+            if (i == 9):
+                print("你在 %d 次内没能猜出结果" % (i + 1))
                 break
 
-        elif num.isdigit()==False:
+        elif num.isdigit() == False:
             print("请输入数字！")
 
-
-
-if (int(num)== set_number):
-    print("答案是：%d" %set_number)
-    print( "你猜对了，你在第 %d 次猜中了数字 ！" %(i+1))
+if (int(num) == set_number):
+    print("答案是：%d" % set_number)
+    print("你猜对了，你在第 %d 次猜中了数字 ！" % (i + 1))
```

</details>

#### 这个文件 ex25.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,7 +1,8 @@
-def  break_words(stuff):
+def break_words(stuff):
     """this function will break up words for us."""
-    words= stuff.split(" ")
+    words = stuff.split(" ")
     return words
+
 
 def sort_words(words):
     """sorts the words."""
@@ -10,27 +11,30 @@
 
 def print_first_word(words):
     """pirints the first word after popping it off."""
-    word=words.pop(0)
+    word = words.pop(0)
     print(word)
+
 
 def print_last_word(words):
     """prints the last word after popping it off."""
-    word= words.pop(-1)
+    word = words.pop(-1)
     print(word)
+
 
 def sort_sentence(sentence):
     """takes in a full sentence and returns the sorted words."""
     return sort_word(words)
 
+
 def print_first_and_last_word(sentence):
     """print the first and the last words of the sentence."""
-    words= break_words(sentence)
+    words = break_words(sentence)
     print_first_word(words)
     print_last_word(words)
 
 
 def print_first_and_last_sorted(sentence):
     """sorts the words then prints the first and the last one."""
-    words=sort_sentence(sentence)
+    words = sort_sentence(sentence)
     print_first_word(words)
     print_last_word(words)
```

</details>

#### 这个文件 ex30.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,21 +1,20 @@
-people=30
-cars=40
-buses=15
+people = 30
+cars = 40
+buses = 15
 
-
-if cars > people :
-    print ("we should take the cars.")
-elif cars < people :
-    print ("we should not take the cars")
+if cars > people:
+    print("we should take the cars.")
+elif cars < people:
+    print("we should not take the cars")
 else:
-    print ("we can't decide.")
+    print("we can't decide.")
 
 if buses > cars:
-    print ("that's too many buses.")
+    print("that's too many buses.")
 elif buses < cars:
-    print ("we still can't decide.")
+    print("we still can't decide.")
 
-if people >buses:
-    print ("alright let's just take the buses.")
+if people > buses:
+    print("alright let's just take the buses.")
 else:
-    print ("fine,let's stay home then.")
+    print("fine,let's stay home then.")
```

</details>

#### 这个文件 ex31.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,24 +1,24 @@
-print ("you enter a dark room with two doors. do you go thorough\
+print("you enter a dark room with two doors. do you go thorough\
 door #1 or door #2?")
 
 door = input(">")
 
-if door =="1":
-    print ("there's a giant bear here eating a cheese cake.\
+if door == "1":
+    print("there's a giant bear here eating a cheese cake.\
     what do you do ?")
-    print ("1.take the cake.")
-    print ("2. scream at the bear.")
+    print("1.take the cake.")
+    print("2. scream at the bear.")
 
-    bear= input(">")
+    bear = input(">")
 
-    if bear =="1":
-        print ("the bear  eats your face off. good job! ")
-    elif bear=="2":
-        print ("the bear eats your legs off. good job!")
+    if bear == "1":
+        print("the bear  eats your face off. good job! ")
+    elif bear == "2":
+        print("the bear eats your legs off. good job!")
     else:
         print("well,doing %s is probably better. bear runs\
-        away.") %bear
-elif door=="2":
+        away.") % bear
+elif door == "2":
     print("you stare into the endless abyss at cthulu's retina.")
     print("1. blueberries")
     print("2. yellow jacket clothespins")
@@ -26,8 +26,8 @@
 
     insantity = input(">")
 
-    if insantity=="1 " or insantity=="2":
-        print( "your body survives powered by a mind of jello\
+    if insantity == "1 " or insantity == "2":
+        print("your body survives powered by a mind of jello\
             good job.")
     else:
         print("the insantity rots your eyes into a pool of muck,\
```

</details>

#### 这个文件 ex32.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,29 +1,29 @@
-the_count=[1,2,3,4]
-fruits=['apples','oranges' ,'pears']
-change=[1,'pennies',2,'dimes',3,'quarters']
+the_count = [1, 2, 3, 4]
+fruits = ['apples', 'oranges', 'pears']
+change = [1, 'pennies', 2, 'dimes', 3, 'quarters']
 
 #this first kind of for-loop goes throught a list
 for number in the_count:
-    print ("this is count %d" % number)
+    print("this is count %d" % number)
 
 #same as  above
 for fruit in fruits:
-    print("a fruit of type %s" %fruit)
+    print("a fruit of type %s" % fruit)
 
 #also we can go through mixed lists thorough
 #notice we have to use %r since we don't know what's init
 for i in change:
-    print("i got %r"  % i)
+    print("i got %r" % i)
 
 #we can also build lists, first start with an empty one
-elements=[]
+elements = []
 
 #then use the range function to do 0 to 5 counts
-for i in range(0,6):
-    print("adding %r to the list."  % i)
+for i in range(0, 6):
+    print("adding %r to the list." % i)
     #append is a funciton that lists understan
-    elements.append(i )
+    elements.append(i)
 
 #now we can print them out too
 for i in elements:
-    print("elements was: %d " %i)
+    print("elements was: %d " % i)
```

</details>

#### 这个文件 ex33.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,17 +1,14 @@
-i=0
-numbers=[]
+i = 0
+numbers = []
 
-while i<6:
-    print("at the top i is %d" %i )
-    numbers.append(i )
-    i=i+1
-    print ("numbers now:",numbers)
-    print("at the bottom i is %d" %i )
-
-
+while i < 6:
+    print("at the top i is %d" % i)
+    numbers.append(i)
+    i = i + 1
+    print("numbers now:", numbers)
+    print("at the bottom i is %d" % i)
 
 print("the numbers:")
 
-
 for num in numbers:
-    print(num )
+    print(num)
```

</details>

#### 这个文件 ex33plus.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,21 +1,22 @@
-i=0
-numbers=[]
-print("input times that you want to loop:" )
-n=input()
-n=int(n )
+i = 0
+numbers = []
+print("input times that you want to loop:")
+n = input()
+n = int(n)
 print("input the number you want to plus ")
-k=input()
-k=int(k)
-
-def while_func(n ):
-    global i
-    while i<n :
-        pass
-        print("at the top i is %d" %i )
-        numbers.append(i)
-        i=i+k
-        print("numbers now:",numbers)
-        print("at the bottom i is %d" %i )
+k = input()
+k = int(k)
 
 
-while_func(n )
+def while_func(n):
+    global i
+    while i < n:
+        pass
+        print("at the top i is %d" % i)
+        numbers.append(i)
+        i = i + k
+        print("numbers now:", numbers)
+        print("at the bottom i is %d" % i)
+
+
+while_func(n)
```

</details>

#### 这个文件 ex33plus3.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,20 +1,19 @@
-n=input("input the times you want to loop:")
-n=int(n)
-k=input("input the nubmers you want to add:")
-k=int(k)
-numbers=[]
-global i,j
-i=0
-j=0
+n = input("input the times you want to loop:")
+n = int(n)
+k = input("input the nubmers you want to add:")
+k = int(k)
+numbers = []
+global i, j
+i = 0
+j = 0
 
-
-for i in range(0,n ):
-    print("at he top i is %d" %i )
-    j=j+k
+for i in range(0, n):
+    print("at he top i is %d" % i)
+    j = j + k
     numbers.append(j)
-    print("numbers now:" ,numbers)
-    print("at the bottom  i is %d" % i )
+    print("numbers now:", numbers)
+    print("at the bottom  i is %d" % i)
 
 print('the numbers:')
 for num in numbers:
-    print (num)
+    print(num)
```

</details>

#### 这个文件 ex34.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,12 +1,12 @@
-animals=['bear','python','peacock','kangaroo','whale','platypus']
+animals = ['bear', 'python', 'peacock', 'kangaroo', 'whale', 'platypus']
 
-print ("the 1st animal is at 0 and is a %r" %animals[0])
-print("the 3rd animal is %r and is at 2" %animals[2])
-print("the animal at 1 is %r and is the 2nd " %animals[1])
-print("the animal at 3 is %r and is the 4th" %animals[3])
-print("the 5th animal is %r and is at 4"%animals[4])
-print("the animal at 2 is %r and is the 3rd "%animals[2])
-print("the 6th animal is %r and is at 5" %animals[5])
-print("the animal at 4 is %r and is the 5th" %animals[4])
+print("the 1st animal is at 0 and is a %r" % animals[0])
+print("the 3rd animal is %r and is at 2" % animals[2])
+print("the animal at 1 is %r and is the 2nd " % animals[1])
+print("the animal at 3 is %r and is the 4th" % animals[3])
+print("the 5th animal is %r and is at 4" % animals[4])
+print("the animal at 2 is %r and is the 3rd " % animals[2])
+print("the 6th animal is %r and is at 5" % animals[5])
+print("the animal at 4 is %r and is the 5th" % animals[4])
 
-print( animals)
+print(animals)
```

</details>

#### 这个文件 ex35.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,46 +1,49 @@
 from sys import exit
 
+
 def gold_room():
-    print ("this room is full of gold. how much \
+    print("this room is full of gold. how much \
     do you take?")
 
-    next =input("> ")
+    next = input("> ")
     if "0" in next or "1" in next:
-        how_much= int(next)
+        how_much = int(next)
     else:
         dead("man ,learn to type a number.")
 
-    if how_much<50:
+    if how_much < 50:
         print("nice,you're not too greedy, you win!")
         exit(0)
     else:
         dead("you greedy bastard!")
+
 
 def bear_room():
     print("there is a bear here")
     print("the bear has a bunch of honey")
     print("the fat bear is in front of another door")
     print("how are you going to move the bear?")
-    bear_moved= False
+    bear_moved = False
 
     while True:
-        next=input(">")
+        next = input(">")
 
-        if next=="take honey":
+        if next == "take honey":
             dead("the bear looks at you then slaps your face off")
-        elif next=="taunt bear" and not bear_moved :
+        elif next == "taunt bear" and not bear_moved:
             print("the bear gets pissed of and chews your legs off")
-        elif next=="open door" and bear_moved:
+        elif next == "open door" and bear_moved:
             glod_room()
         else:
             print("i got no idea what that means")
+
 
 def cthulhu_room():
     print("here you see the great evil cthulhu")
     print("he ,it , whatever stares at you and you go insane")
     print("do yo flee for your life or eat your head?")
 
-    next=input(">")
+    next = input(">")
 
     if "flee" in next:
         start()
@@ -49,22 +52,25 @@
     else:
         cthulhu_room()
 
+
 def dead(why):
-    print (why,"good job!")
+    print(why, "good job!")
     exit(0)
+
 
 def start():
     print("you are in a dark room")
     print("there is a door to your right and left")
     print("which one do yo take")
 
-    next= input(">")
+    next = input(">")
 
-    if next== "left":
+    if next == "left":
         bear_room()
-    elif next=="right":
+    elif next == "right":
         cthulhu_room()
     else:
         dead("you stumble around the room until you starve")
 
+
 start()
```

</details>

#### 这个文件 ex39.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,5 +1,4 @@
-ten_things="apples oranges crows telephone light sugar"
-
+ten_things = "apples oranges crows telephone light sugar"
 
 print("wait there's not 10 things in that\
 list, let's fix that")
@@ -8,20 +7,20 @@
 more_stuff=["day","night","song","frisbee","corn",\
 "banana","girl","boy"]
 
-while len(stuff) !=10:
-    next_one=more_stuff.pop()
-    print("adding:",next_one)
+while len(stuff) != 10:
+    next_one = more_stuff.pop()
+    print("adding:", next_one)
     stuff.append(next_one)
-    print("there's %d items now." %len(stuff))
+    print("there's %d items now." % len(stuff))
 
-print("there we go:",stuff)
+print("there we go:", stuff)
 
 print("let's do some things with stuff.")
 
-print( stuff[1])
-print(stuff[-1]) #whoa ! fance
+print(stuff[1])
+print(stuff[-1])  #whoa ! fance
 print(stuff.pop())
-print(''.join(stuff)) #what ? cool!
-print('#'.join(stuff[3:5])) #super stellar!
+print(''.join(stuff))  #what ? cool!
+print('#'.join(stuff[3:5]))  #super stellar!
 
 print(stuff[3:6])
```

</details>

#### 这个文件 ex40.py:

<details>
<summary>More details</summary>

```diff
--- 
+++ 
@@ -1,23 +1,26 @@
 cities={'CA':'San Francisco','MI':'Detroit',\
 'FL':'Jacksonville'}
 
-cities['NY']='New York'
-cities['OR']='Portland'
+cities['NY'] = 'New York'
+cities['OR'] = 'Portland'
 
-def find_city(themap,state):
+
+def find_city(themap, state):
     if state in themap:
         return themap[state]
     else:
         return "not found"
 
+
 #ok pay attention!
 cities['_find'] = find_city
 
 while True:
-    print("state? (enter to quit)",)
-    state=input("> ")
+    print(
+        "state? (enter to quit)", )
+    state = input("> ")
     if not state: break
 
-#this line is the most important ever! study!
-    city_found =cities['_find'](cities,state)
+    #this line is the most important ever! study!
+    city_found = cities['_find'](cities, state)
     print(city_found)
```

</details>


## 2. 代码相似问题：
### 这些代码非常相似，建议抽象：

#### ex25.py 文件中的 26 至 30 行：
```python
    """print the first and the last words of the sentence."""
    words= break_words(sentence)
    print_first_word(words)
    print_last_word(words)

```

#### ex25.py 文件中的 33 至 37 行：
```python
    """sorts the words then prints the first and the last one."""
    words=sort_sentence(sentence)
    print_first_word(words)
    print_last_word(words)
```

## 3. 复杂度及其他问题：
#### 文件 ex35.py 的 19-36 行
函数 `bear_room` Cyclomatic complexity(循环复杂度、条件复杂度)为 (7)，过高、建议缩减
