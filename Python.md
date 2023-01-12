# Python

## 目录

 [TOC]

## 计算机基本知识

 你可以把计算机看成一堆**硬件**组成的集合

 这些硬件之间相互联系,相互依赖

 管理这些硬件的是**操作系统**

 而程序是写在操做系统上的

 所以就有这么一个大小关系

 计算机本身操作系统程序

 内存,CPU,硬盘是计算机的核心

 在运行程序时

 1. 硬盘里的数据会给内存
 2. 内存与CPU进行交互,内存发送数据给CPU,让他处理,处理完在给内存
 3. 程序运行完,操作系统回收内存(Python的流程)

 ```mermaid
 graph TB
 计算机{计算机}
 操作系统{{操作系统}}
 
 
 操作系统==>程序通过操作系统控制==>计算机
 操作系统-->硬盘[硬盘]
 操作系统-->内存[内存]
 操作系统-->CPU[CPU]
 app((程序))
 app-.不能直接操作.-计算机
 app==>建立在==>操作系统
 
 硬盘-->运行时-->将数据移到-->内存
 内存-->存储程序的数据-->将数据给-->CPU
 CPU-->处理程序数据然后返回-->内存
 内存-->将程序数据返回-->硬盘
 操作系统-->回收程序-->内存
 CPU-->根据程序指令操作数据操作数据-->硬盘
 
 计算机-->内存
 计算机-->CPU
 计算机-->硬盘
 ```
 ## 变量
 格式: 变量名=数据

 ```python
 a=1
 #定义了一个a的变量
 b=1
 #定义了一个b的变量
 
 #以上变量都为int类型
 ```

 以上例子的数据类型为整数(整型)

 ```python
 a="我是Installation"
 #定义了一个文本类型变量(字符串)
 ```

 |  数据类型  | 对应关键字                       |
 | :--------: | -------------------------------- |
 |  文本类型  | `str`                            |
 |  数值类型  | `int` `float` `complex`          |
 |  序列类型  | `list` `tuple` `range`           |
 |  映射类型  | `dict`                           |
 |  集合类型  | `set` `frozenset`                |
 |  布尔类型  | `bool`                           |
 | 二进制类型 | `bytes` `bytearray` `memoryview` |

 记住关键的**int整型,str字符型**

## 函数

 前面讲到程序就是**数据**和**函数**,调用函数修改数据就是编程本质

 函数可以理解为一个**方法**(在类里面就叫做方法,在类外才叫做函数),里面放一些代码,可以被重复调用

 调用函数是会执行函数里面的代码

 创建函数格式:def 函数名(参数):

 1. 参数可以不填,尤其记住后面要有一个**冒号**
 2. 标点符号必须是英文
 3. 写在函数体里面的代码前面必须有缩进(一个Tab的长度)

 调用格式:函数名(参数)

 1. 与创建函数一样标点符号必须是英文
 2. 调用函数时不用在前面加缩进

 ```python
 def helloworld():
     #定义一个函数,作用是打印Hello World
     print("Hello World")
 #调用这个函数
 helloworld()
 
 Hello World
 ```

 - ## 参数

   在调用函数时，通常会传递参数，函数内部的代码保持不变，针对 **不同的参数 处理 不同的数据**

   有位置传参、关键字传参、默认值参数、多值参数等

   - **形参**：**定义** 函数时的 参数变量
   - **实参**：**调用** 函数时，使用的参数变量

   参数传递的过程，就是 把实参的引用 传递给 形参 ，使用实参的值来执行函数体的过程

   在 `Python` 中，函数的 **实参**/**返回值** 都是是靠 **引用** 来传递来的

   ### 1 . 位置实参

   按照参数位置，依次传递参数，这是最普通的方式

   ```python
   def sum(a, b)
       print(a + b)
                                                                     
   sum(3, 9)
   #调用函数时，按顺序传递参数，3 传给 a，9 传给 b
                                                                     
   12
   ```

   ### 2 . 如果不想按照顺序传递参数，也可以按关键字传递,效果一样

   ```python
   def sum(a, b)
       print(a + b)
                                                                     
   sum(b = 3, a = 9)
   #调用函数时，按关键字传递参数，3 传给 b，9 传给 a
                                                                     
   12
   ```

   以上两种最常见,其余后文会说到

   - ## 返回值

      在函数体内写return关键字,后面写返回内容
     
      格式: return 返回内容
     
      - 返回的内容可以是任何数据类型
      - 返回的内容可以是函数(装饰器会讲)
      - 写了返回后return后面的代码不会执行
      
      ```python
      def sum(a, b)
          return a+b
      
      print(location(3,9))
      #调用函数时传入参数,然后返回a+b
      
      12
      ```
     
      ```python
      def booltest()
          return True
      
      print(booltest())
      #返回值也可以是bool类型
      
      True
      ```

## 开发工具

 - ## PyCharm

   PyCharm是一种[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink) [IDE](https://baike.baidu.com/item/IDE/8232086?fromModule=lemma_inlink)（Integrated Development Environment，集成开发环境），带有一整套可以帮助用户在使用[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink)语言开发时提高其效率的工具，比如[调试](https://baike.baidu.com/item/调试/5852756?fromModule=lemma_inlink)、[语法高亮](https://baike.baidu.com/item/语法高亮/9686751?fromModule=lemma_inlink)、[项目管理](https://baike.baidu.com/item/项目管理/85389?fromModule=lemma_inlink)、代码跳转、智能提示、[自动完成](https://baike.baidu.com/item/自动完成/22748028?fromModule=lemma_inlink)、[单元测试](https://baike.baidu.com/item/单元测试/1917084?fromModule=lemma_inlink)、[版本控制](https://baike.baidu.com/item/版本控制/3311252?fromModule=lemma_inlink)此外，该IDE提供了一些高级功能，以用于支持[Django](https://baike.baidu.com/item/Django/61531?fromModule=lemma_inlink)框架下的专业[Web](https://baike.baidu.com/item/Web/150564?fromModule=lemma_inlink)开发

 

   PyCharm是最受Python程序员喜爱的Python编辑器,本人**推荐使用这个**

   但是专业版收费,具体信息去[官网](https://www.jetbrains.com/pycharm/)查看

 - ## Visual Studio Code

   Visual Studio Code（简称“VS Code”）是Microsoft在2015年4月30日[Build](https://baike.baidu.com/item/Build/15992854?fromModule=lemma_inlink)开发者大会上正式宣布一个运行于 [MacOS](https://baike.baidu.com/item/Mac OS X/470629?fromModule=lemma_inlink)、[Windows](https://baike.baidu.com/item/Windows?fromModule=lemma_inlink)和[ Linux](https://baike.baidu.com/item/ Linux/27050?fromModule=lemma_inlink) 之上的，针对于编写现代[Web](https://baike.baidu.com/item/Web/150564?fromModule=lemma_inlink)和[云应用](https://baike.baidu.com/item/云应用/476249?fromModule=lemma_inlink)的跨平台[源代码编辑器](https://baike.baidu.com/item/源代码编辑器/16273015?fromModule=lemma_inlink)可在桌面上运行，并且可用于[Windows](https://baike.baidu.com/item/Windows/165458?fromModule=lemma_inlink)，[macOS](https://baike.baidu.com/item/macOS/8654551?fromModule=lemma_inlink)和[Linux](https://baike.baidu.com/item/Linux/27050?fromModule=lemma_inlink)

   它具有对[JavaScript](https://baike.baidu.com/item/JavaScript/321142?fromModule=lemma_inlink)，[TypeScript](https://baike.baidu.com/item/TypeScript/4314718?fromModule=lemma_inlink)和[Node.js](https://baike.baidu.com/item/Node.js/7567977?fromModule=lemma_inlink)的内置支持，并具有丰富的其他语言（例如[C++](https://baike.baidu.com/item/C%2B%2B/99272?fromModule=lemma_inlink)，[C＃](https://baike.baidu.com/item/C＃/195147?fromModule=lemma_inlink)，[Java](https://baike.baidu.com/item/Java/85979?fromModule=lemma_inlink)，[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink)，[PHP](https://baike.baidu.com/item/PHP/9337?fromModule=lemma_inlink)，[Go](https://baike.baidu.com/item/Go/953521?fromModule=lemma_inlink)）和运行时（例如[.NET](https://baike.baidu.com/item/.NET/156737?fromModule=lemma_inlink)和[Unity](https://baike.baidu.com/item/Unity/10793?fromModule=lemma_inlink)）扩展的[生态系统](https://baike.baidu.com/item/生态系统/457895?fromModule=lemma_inlink)

 

   Visual Studio Code几乎可以写**任何编程语言**,当然用来写Python也是不错的

   它的体积比PyCharm小,但是Visual Studio Code终究还是一个编辑器,无法与IDE相提并论

   具体信息去[官网](https://code.visualstudio.com/)查看

 - ## Sublime Text

   Sublime Text 是一个文本[编辑器](https://baike.baidu.com/item/编辑器/9067697?fromModule=lemma_inlink)（收费[软件](https://baike.baidu.com/item/软件/12053?fromModule=lemma_inlink)，可以无限期试用），同时也是一个先进的[代码](https://baike.baidu.com/item/代码/86048?fromModule=lemma_inlink)编辑器Sublime Text是由程序员Jon Skinner于2008年1月份所开发出来，它最初被设计为一个具有丰富扩展功能的[Vim](https://baike.baidu.com/item/Vim?fromModule=lemma_inlink)

   Sublime Text具有漂亮的用户界面和强大的功能，例如代码缩略图，[Python](https://baike.baidu.com/item/Python?fromModule=lemma_inlink)的插件，代码段等还可自定义键绑定，菜单和工具栏Sublime Text 的主要功能包括：拼写检查，书签，完整的 [Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink) API, 即时项目切换，多选择，多窗口等等[Sublime](https://baike.baidu.com/item/Sublime/8130415?fromModule=lemma_inlink) Text 是一个跨平台的编辑器，同时支持Windows、[Linux](https://baike.baidu.com/item/Linux?fromModule=lemma_inlink)、[MacOS](https://baike.baidu.com/item/Mac OS X?fromModule=lemma_inlink)等操作系统

 

   这是一款不错的Python开发工具,但与前两者相比个人感觉比不上

   具体信息去[官网](https://www.sublimetext.com/)查看

 具体使用哪个看个人需求,另外安装了工具还要装Python解释器

 ```mermaid
 pie
     title 使用Python各个开发工具人数占比
     "Pycharm" : 50
     "Visual Studio Code" : 20
     "Sublime Text" : 10
     "其他":1
 ```

 

 - ## Python安装

   下表复制Python官网**3.9.2**安装列表根据需求进行下载

   一般如果你是Windows操作系统直接点最后一个

   |                             版本                             | 操作系统 |
   | :----------------------------------------------------------: | :------: |
   | [压缩源码包](https://www.python.org/ftp/python/3.9.2/Python-3.9.2.tgz) |   源码   |
   | [XZ 压缩源压缩包](https://www.python.org/ftp/python/3.9.2/Python-3.9.2.tar.xz) |   源码   |
   | [macOS 64 位英特尔安装程序](https://www.python.org/ftp/python/3.9.2/python-3.9.2-macosx10.9.pkg) |   Mac    |
   | [macOS 64 位通用2 安装程序](https://www.python.org/ftp/python/3.9.2/python-3.9.2-macos11.pkg) |   Mac    |
   | [Windows 嵌入式程序包（32 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2-embed-win32.zip) | Windows  |
   | [Windows 嵌入式程序包（64 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2-embed-amd64.zip) | Windows  |
   | [Windows帮助文件](https://www.python.org/ftp/python/3.9.2/python392.chm) | Windows  |
   | [Windows安装程序（32 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2.exe) | Windows  |
   | [Windows安装程序（64 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2-amd64.exe) | Windows  |

   **双击安装包随后按照步骤来安装(照片是3.10.8的安装,给出的链接是3.9.2的,步骤都一样)**

 <img alt ="python安装步骤" src="https://599575461.github.io/Teaching/img/Install_python.png" style="zoom:100%;" /

 等待安装成功,看见**Successfully**表示成功安装

## 编码

 一段中文他的编码是怎样的的,如何去解码,都会影响结果

 <img alt = "GB 2312解码" src = "https://599575461.github.io/Teaching/img/en.png" style="zoom:100%;" /GB 2312解码

 <img alt = "UTF-8解码" src ="https://599575461.github.io/Teaching/img/dn.png" style="zoom:100%;" /UTF-8解码

 不同的解码方式就会早就不同的结果

 文本原本是UTF-8编码,现在用GB 2312解码就会变成图1的结果

 如果文本是GB 2312编码的,用UTF-8解码也会出现与原本不一样的结果

 这种出现不一样结果的叫做**乱码**

 这种用不同编码解码编码的就是最简单的文本加密系统

 现在有一段文本为"鑰侀腑浣燷"

 我们无法解读出来这就做**加密**

 然后我们使用UTF-8解码,获得的文本为"老鸭你"d

 这种把我们看不懂的转换成我们看得懂的叫做**解密**

 当然,这是最简单的加密和解密,常用的加密解密方式有MD5,ASE等

 对于编码,只需要知道Python使用UTF-8编码,这也是使用最广泛的编码之一

## 数组与字典

 - ### 数组

   数组用于在单个变量中存储多个值

   格式:数组名=[]

   ```python
   a=[]
   #创建了一个a数组
   ```

   初始化数组

   ```python
   a=['banana','apple']
   #在数组里面写了banana和apple
   ```

   访问数组使用下标

   ```python
   a=['banana','apple']
   print(a[0])
   print(a[1])
                                               
   banana
   apple
   ```

   数组的第一位用下标0来表示以此类推

   使用 `len()` 方法来返回数组的长度（数组中的元素数量）

   ```python
   a=['banana','apple']
   x = len(a)
   #返回 a 数组中的元素数量
                                               
   2
   ```

   **注意：**数组长度总是比最高的数组索引大一个

   ## 添加数组元素

   您可以使用 `append()` 方法把元素添加到数组中

   向 cars 数组再添加一个元素：

   ```python
   a=['banana','apple']
   a.append("Audi")
   print(a)
                                               
   ['banana','apple','Audi']
   ```

   **其余数组操作看下表**

   | 方法                                                         | 描述                                                 |
   | :----------------------------------------------------------- | :--------------------------------------------------- |
   | [append()](https://www.w3school.com.cn/python/ref_list_append.asp) | 在列表的末尾添加一个元素                             |
   | [clear()](https://www.w3school.com.cn/python/ref_list_clear.asp) | 删除列表中的所有元素                                 |
   | [copy()](https://www.w3school.com.cn/python/ref_list_copy.asp) | 返回列表的副本                                       |
   | [count()](https://www.w3school.com.cn/python/ref_list_count.asp) | 返回具有指定值的元素数量                             |
   | [extend()](https://www.w3school.com.cn/python/ref_list_extend.asp) | 将列表元素（或任何可迭代的元素）添加到当前列表的末尾 |
   | [index()](https://www.w3school.com.cn/python/ref_list_index.asp) | 返回具有指定值的第一个元素的索引                     |
   | [insert()](https://www.w3school.com.cn/python/ref_list_insert.asp) | 在指定位置添加元素                                   |
   | [pop()](https://www.w3school.com.cn/python/ref_list_pop.asp) | 删除指定位置的元素                                   |
   | [remove()](https://www.w3school.com.cn/python/ref_list_remove.asp) | 删除具有指定值的项目                                 |
   | [reverse()](https://www.w3school.com.cn/python/ref_list_reverse.asp) | 颠倒列表的顺序                                       |
   | [sort()](https://www.w3school.com.cn/python/ref_list_sort.asp) | 对列表进行排序                                       |

   - ### 字典

     字典是一个无序、可变和有索引的集合,在 Python 中，字典用花括号编写，拥有键和值

     格式:字典名 = {键:值,键:值}

     ### 

     创建并打印字典：

     ```python
     thisdict =	{
       "brand": "Porsche",
       "model": "911",
       "year": 1963
     }
     print(thisdict)
                                                                                             
     {
       "brand": "Porsche",
       "model": "911",
       "year": 1963
     }
     ```

     ## 访问项目

     您可以通过在方括号内引用其键名来访问字典的项目：

     ### 

     获取 "model" 键的值：

     ```python
     x = thisdict["model"]
     ```

     还有一个名为 `get()` 的方法会给你相同的结果：

     ### 

     获取 "model" 键的值：

     ```python
     x = thisdict.get("model")
     ```

     ## 更改值

     您可以通过引用其键名来更改特定项的值：

     ### 

     把 "year" 改为 2019：

     ```python
     thisdict =	{
       "brand": "Porsche",
       "model": "911",
       "year": 1963
     }
     thisdict["year"] = 2019
     ```

     Python 提供一组可以在字典上使用的内建方法

     | 方法                                                         | 描述                                               |
     | :----------------------------------------------------------- | :------------------------------------------------- |
     | [clear()](https://www.w3school.com.cn/python/ref_dictionary_clear.asp) | 删除字典中的所有元素                               |
     | [copy()](https://www.w3school.com.cn/python/ref_dictionary_copy.asp) | 返回字典的副本                                     |
     | [fromkeys()](https://www.w3school.com.cn/python/ref_dictionary_fromkeys.asp) | 返回拥有指定键和值的字典                           |
     | [get()](https://www.w3school.com.cn/python/ref_dictionary_get.asp) | 返回指定键的值                                     |
     | [items()](https://www.w3school.com.cn/python/ref_dictionary_items.asp) | 返回包含每个键值对的元组的列表                     |
     | [keys()](https://www.w3school.com.cn/python/ref_dictionary_keys.asp) | 返回包含字典键的列表                               |
     | [pop()](https://www.w3school.com.cn/python/ref_dictionary_pop.asp) | 删除拥有指定键的元素                               |
     | [popitem()](https://www.w3school.com.cn/python/ref_dictionary_popitem.asp) | 删除最后插入的键值对                               |
     | [setdefault()](https://www.w3school.com.cn/python/ref_dictionary_setdefault.asp) | 返回指定键的值如果该键不存在，则插入具有指定值的键 |
     | [update()](https://www.w3school.com.cn/python/ref_dictionary_update.asp) | 使用指定的键值对字典进行更新                       |
     | [values()](https://www.w3school.com.cn/python/ref_dictionary_values.asp) | 返回字典中所有值的列表                             |

## If,for语句

 if就是判断是否为真,为真就执行if下的代码

 ```python
 if True:
 	print("True")
 
 True    
 ```

 ==运行判断两个变量是否相等,相等返回True,不相等返回false

 ```python
 a=1
 b=1
 #如果a=b就打印a=b
 if a==b:
 	print("a=b")
 
 a=b    
 ```

 if里面的语句执行结束会执行if后面的

 ```python
 a=1
 b=1
 #如果a=b就打印a=b
 if a==b:
      print("a=b")
      #if里面的运行结束打印if finish
      print("if finish")
 
 a=b
 if finish
 ```

 if判断的条件为假则继续

 以下为if的流程图:

 ````mermaid
 graph LR
 start(开始)-->if{条件}
 if-->yes(True)
 yes-->yes_num[条件代码]
 if-->no(False)
 
 yes_num-->if_finid(if后的代码)
 no-->if_finid
 ````

 - ## if-else

   以下为if-else的流程图:

   ```mermaid
   graph LR
   start(开始)-->if{条件}
   if-->yes(True)
   yes-->yes_num[条件代码]
   if-->no(False)
   no-->else((else))
                                               
   yes_num-->if_finid(if后的代码)
   else-->if_fini_else(else中的代码)
   if_fini_else-->if_finid
   ```

 

   ```python
 a=1
 b=2
 
 if a==b :
 	print("a=b")
 #这里的else等于if a!=b:
 else:
 	#!=就是不等于
 	print("a!=b")
 
 a!=b
   ```
 - ## if-elif

   以下为if-elif的流程图:

   ```mermaid
   graph LR
   start(开始)-->if{条件}
   if-->yes(True)
   yes-->yes_num[条件代码]
   if-->no(False)
   no-->elif{{elif条件}}
   elif-->true1(True)
   elif-->false1(False)

   true1-->elif代码(elif代码)
   false1-->elif1{{elif条件2}}
   elif1-->true2(True)
   true2-->elif5(elif2代码)
   elif1-->false2(False)
   false2-->num(....)

   yes_num-->if_finid(if后的代码)
   ```

   ```python
   a=1
   b=2
   if a==b :
   	print("a=b")
   elif ba:
   	print("ba")
   elif b<a:
       print("b<a")

   ```

 - ## for

 `for` 循环用于迭代序列（即列表，元组，字典，集合或字符串）

 这与其他编程语言中的 `for` 关键字不太相似，而是更像其他面向对象编程语言中的迭代器方法

 通过使用 `for` 循环，我们可以为列表、元组、集合中的每个项目等执行一组语句

 打印 fruits 列表中的每种水果：

 ```python
fruits = ["apple", "banana", "cherry"]
 for x in fruits:
     print(x)
 ```

 **提示：**`for` 循环不需要预先设置索引变量

 ## 循环遍历字符串

 甚至连字符串都是可迭代的对象，它们包含一系列的字符：

 循环遍历单词 "banana" 中的字母：

 ```python
for x in "banana":
 	print(x)
 ```

 ## break 语句

 通过使用 `break` 语句，我们可以在循环遍历所有项目之前停止循环：

 如果 x 是 "banana"，则退出循环：

 ```python
fruits = ["apple", "banana", "cherry"]
 for x in fruits:
    print(x) 
     if x == "banana":
        break
 ```

 当 x 为 "banana" 时退出循环，但这次在打印之前中断：

 ```python
 fruits = ["apple", "banana", "cherry"]
 for x in fruits:
    if x == "banana":
         break
    print(x)
 ```

 ## continue 语句

 通过使用 `continue` 语句，我们可以停止循环的当前迭代，并继续下一个：

 不打印香蕉：

 ```python
fruits = ["apple", "banana", "cherry"]
 for x in fruits:
  if x == "banana":
     continue
  print(x)
 ```

 - ## range() 函数

 如需循环一组代码指定的次数，我们可以使用 `range()` 函数，

 `range()` 函数返回一个数字序列，默认情况下从 0 开始，并递增 1（默认地），并以指定的数字结束

 使用 `range()` 函数：

 ```python
for x in range(10):
   print(x)
 ```

**注意：**`range(10)` 不是 0 到 10 的值，而是值 0 到 9

`range()` 函数默认 0 为起始值，不过可以通过添加参数来指定起始值：`range(3, 10)`，这意味着值为 3 到 10（但不包括 10）：

使用起始参数：

```python
 for x in range(3, 10):
   print(x)
```

`range()` 函数默认将序列递增 1，但是可以通过添加第三个参数来指定增量值：`range(2, 30, 3)`：

使用 3 递增序列（默认值为 1）：

```python
 for x in range(3, 50, 6):
  print(x)
```

 - ## For 循环中的 Else

 for 循环中的 `else` 关键字指定循环结束时要执行的代码块：

打印 0 到 9 的所有数字，并在循环结束时打印一条消息：

```python
 for x in range(10):
  print(x)
 else:
  print("Finally finished!")
```

 - ## 嵌套循环

嵌套循环是循环内的循环

“外循环”每迭代一次，“内循环”将执行一次：

打印每个水果的每个形容词：

```python
 adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]
 
 for x in adj:
   for y in fruits:
     print(x, y)
```

## pass 语句

for 语句不能为空，但是如果您处于某种原因写了无内容的 for 语句，请使用 pass 语句来避免错误

```python
 for x in [0, 1, 2]:
  pass
```

## 面向对象

 学习面向对象之前建议先去看[**面向过程&面向对象**](#面向过程&面向对象)这一节

 **面向对象是高级编程语言的重点**

 面向对象程序设计以对象为核心，该方法认为程序由一系列对象组成

 类是对现实世界的抽象，包括表示静态属性的数据和对数据的操作，对象是类的化 对象间通过消息传递相互通信，来模拟现实世界中不同实体间的联系 在面向对象的程序设计中，对象是组成程序的基本模块

 通俗点就是**变量和函数的整合**

 面向对象三大基本特征：**封装、继承、多态**(这些以后会讲)

 而面向对象的过程就是找对象、建立对象、使用对象、维护对象的关系的过程

 这么说可能有点抽象,举个例子

 一只猫,他有年龄,名字和行为

 知道毛的**年龄,名字和行为**就可以**造出一个猫**出来(实列化对象)

 格式:class 类名(继承的类):

 继承后面会学,继承的类可以不填

 ```python
 class Cat: 
 #创建猫类														
 	name = '' #猫有名字
 	age = 0 #猫有年龄
 def run():
        print("这只猫正在跑")
 cat1 = Cat() #造出一个猫出来
 cat1.run() # 这只猫正在跑
 
 这只猫正在跑
 ```

---

 ### 封装

 写在类里面的函数的第一个参数是self(顾名思义,就是自己的意思)

 ```python
 class Test():
 #创建一个类
     def __init__(self):
         pass
 
     #创建一个在类里面的函数(方法)
     def printhello(self):
           print("hello world")
 #实列化对象
 p=Test()
 #执行类里面的函数
 p.printhello()
 
 hello world
 ```

 在类中定义\_\_init\_\_函数(构造函数),在执行p=People()是会执行\_\_init\_\_函数里的代码(实列化对象)

 ```python
 class Test():
 #创建一个类
     def __init__(self):
         print("调用构造函数")
 
     #创建一个在类里面的函数(方法)
     def printhello(self):
         print("hello world")
 #实列化对象,这时就是执行"__init__"这个函数里面的内容
 p=Test()
 #执行类里面的函数
 p.printhello()
 
 调用构造函数
 hello world
 ```

 在实列化对象的时候传的参数是构造函数接收

 ```python
 class Test():
 #创建一个类
     def __init__(self,num):
         print(num)
 
     #创建一个在类里面的函数(方法)
     def printhello(self):
         print("hello world")
 #实列化对象,这时就是执行"__init__"这个函数里面的内容
 # 传入'hello'给构造函数的num
 p=Test('hello')
 #执行类里面的函数
 p.printhello()
 
 hello
 hello world
 ```

 在封装类需定义变量时加上"self."

 ```python
 class Test():
 #创建一个类
     def __init__(self,num):
         self.num = num #定义类里面的num等于传入的num
 
     # 创建一个在类里面的函数(方法)
     # 方法可以直接使用num(前面也要加self.)
     def printhello(self):
         print(self.num)
 #实列化对象,这时就是执行"__init__"这个函数里面的内容
 # 传入'hello'给构造函数的num
 p=Test('hello')
 #执行类里面的函数
 p.printhello()
 
 hello
 
 ```
---
 ### 继承

 现在有两个类

 A类和B类,我想让B类获得A类的**方法**和**属性**

 现在就要用到**继承**

 继承格式:**class 类名(继承的类):**

 ```python
 class A():
 # 定义一个A类
 	# 构造函数
  def __init__(self,num):
      # 创建self.num
        self.num = num 
  def test(self):
        print('A类test方法')
 
 class B(A):
 # 定义一个B类,继承B类
 	pass
 
 b = B() # 化一个B类
 b.test() # 可以调用A类的方法
 
 A类test方法
 ```

 Python中有个类叫**Object**,这是Python自带的类

 一个类如果继承了他就会有更多方法

 Python中还能实现多继承

 ```python
 class A():
 # 定义一个A类
 	# 构造函数
        def __init__(self):
          pass
        def test(self):
          print('A类test方法')
 class C():
     # 定义一个C类
        def __init__(self):
          pass
        def test_C(self):
          print('C类test方法')
 class B(A,C):
 # 定义一个B类,继承B类
     	pass
 
 b = B() # 化一个B类
 b.test() # 可以调用A类的方法
 b.test_C() # 可以调用C类的方法
 
 A类test方法
 C类test方法
 ```

 

## 面向过程&面向对象

 现在,你想要做炒菜

 你是不是要这样做

 1. 买菜
 2. 切菜
 3. 把菜放进锅里
 4. 炒菜
 5. 把菜搞出来
 6. 放进碗里
 7. 做好了菜

 这种注重**过程**的就是**面向过程**

 但是你也可以这样做

 1. 买菜
 2. 把菜扔进自动炒菜机里
 3. 做好了菜

 这种注重**结果**的就是**面向对象**

 面向对象你不需要知道自动炒菜机的原理,你只需要知道怎么**用**自动炒菜机

 而面向过程就必须知道做菜的原理

 现在把做菜想象成编程

 面向对象:写代码时不需要把所有功能都写进自己的代码,而是拆分成很多模块,一个模块用一个工具实现,另一个自己写,另一个再用工具实现

 面向过程:写代码时把几乎所有的功能都在**自己写的代码**里实现

 在简略点就是面向对象某些功能使用面向过程解决,面向过程则全部都自己解决

 优缺点:面向对象的语言**开发周期短**语法相对于面向过程的语言**更加简单**,也是众多高级编程语言的特性

 但是面向对象的语言运行效率常常比面向过程**更低**

 C语言就是典型的**面向过程**的语言

 C++在C语言的基础上引入**面向对象**和一些工具从而使得C++被称为编程界的**万金油**,但是运行效率是比C语言低的

 总的来说现在编程**主要偏向面向对象**

## 异常

 也许你会在pycharm中看到这样的报错

 <img src = "https://599575461.github.io/Teaching/img/Try_0.png"

 先逐一分析一下

 <img src = "https://599575461.github.io/Teaching/img/Try_1.png"

 可以看到其实最主要的就是**错误类型**和**错误原因**

 而我们想要捕获到这个错误就要用到try语句

 ```python
 a=[1,2] #定义一个a列表
 # print(a[2]) #我们去索引a的第三个数，会报错
 # IndexError: list index out of range
 try:#现在我们用try捕获错误
     print(a[2])
 except IndexError:#用except捕获IndexError错误
     print("索引错误")
 
 索引错误
 ```

 在执行完except后会执行finally语句,进行回收

 ```python
 a=[1,2] #定义一个a列表
 # print(a[2]) #我们去索引a的第三个数，会报错
 # IndexError: list index out of range
 try:#现在我们用try捕获错误
     print(a[2])
 except IndexError:#用except捕获IndexError错误
     print("索引错误")
 finally:
     print("OK")
     
 索引错误
 OK
 ```

## 解析式

 解析式往往是区分小白和大佬的最好方法

 解析式往往能把复杂冗余的代码浓缩成几行

 ### 列表解析式

 现在我们想要在列表里面存1-100这些数

 我们不可能去手写

 正确的写法为利用for循环

 ```python
 a = [] #定义a列表
 for i in range(1, 100):
     a.append(i) # 循环1-100,添加到末尾
 print(a)
 
 [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23....]
 ```

 这样写可以，很标准，但是比较冗余，足足花了4行代码来写!!!!

 现在来看列表解析式

 ```python
 a = [i for i in range(1, 100)]
 print(a)
 
 [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23....]
 ```

 更加的简洁美观

 现在可以把他搞成一行，效果一样

 ```python
 print([i for i in range(1, 100)])
 
 [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23....]
 ```

 现在我们想要获得1-100中的所有偶数

 标准for写法

 ```python
 a = [] #定义a列表
 for i in range(1, 100):
     if i % 2 == 0: # 循环1-100,如果除以2的余数为0就添加到末尾
         a.append(i)
 print(a)
 
 [2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32...]
 ```

 现在来看列表解析式

 ```python
 a = [i for i in range(1, 100) if i % 2 == 0]
 print(a)
 ```

 if写在后面，这样写更加的美观，易懂

 现在将所有的数都转化成str类型

 ```python
 a = [str(i) for i in range(1, 100) if i % 2 == 0]
 print(a)
 
 ['2', '4', '6', '8', '10', '12', '14', '16', '18', '20', '22', '24', '26', '28', '30', '32'...]
 ```

 通过这种写法我们还可以完成很多操作，这里不多说

## Pythonic语法

 这是遍历的标准写法

 ```python
 a=[1,2,3,4]
 for i in range(len(a)):
     print(a[i])
     
 1
 2
 3
 4
 ```

 这种是利用下标获得列表的数据

 但是利用Pythonic语法会变得更加简洁，美观

 ```python
 a=[1,2,3,4]
 for i in a:
     print(a)
 
 1
 2
 3
 4
 ```

 这是文件操作的标准写法

 ```python
 f = open("test.txt",'w+') # 用w+模式打开创建文件
 f.write("test")
 f.close()
 ```

 但是利用Pythonic语法会变得更加简洁，美观

 ```python
 with open("test.txt",'w+'):
     f.write("test")
 # 他会自动清理
 ```

## OS,Json库的使用

 os是Python的一个内置库

 这个模快提供了一个便携的方式去使用操作系统的相关功能

 ## OS

 了解**OS**的一些常用语句

 使用前要先import os

 1. os.getcwd() 当前工作目录

 2. os.uname()

    返回标识当前操作系统的信息。返回值是一个具有五个属性的对象：

    - `sysname` - 操作系统名称
    - `nodename` - 网络上机器的名称（实施定义）
    - `release` - 操作系统版本
    - `version` - 操作系统版本
    - `machine` - hardware identifier

 3. os.mkdir(*path*, mode)

    创建一个名称为*path*的目录，模式为*mode*。

    如果该目录已经存在，则会出现异常FileExistsError

 4. os.makedirs(name, mod, exist_ok=False)

    递归创建目录和os.mkdir差不多，但是会生成所有中间目录以及叶子目录

 了解**os.path**的一些常用语句

 | os.path.abspath(path)              | 返回绝对路径                                                 |
 | :--------------------------------- | :----------------------------------------------------------- |
 | **os.path.basename(path)**         | **返回文件名**                                               |
 | os.path.commonprefix(list)         | 返回list(多个路径)中，所有path共有的最长的路径               |
 | os.path.dirname(path)              | 返回文件路径                                                 |
 | **os.path.exists(path)**           | **如果路径 path 存在，返回 True；如果路径 path 不存在或损坏，返回 False** |
 | os.path.lexists(path)              | 路径存在则返回 True，路径损坏也返回 True                     |
 | os.path.expanduser(path)           | 把 path 中包含的 ~ 和 ~user 转换成用户目录                   |
 | os.path.expandvars(path)           | 根据环境变量的值替换 path 中包含的 name                      |
 | os.path.getctime(path)             | 返回文件 path 创建时间                                       |
 | os.path.getsize(path)              | 返回文件大小，如果文件不存在就返回错误                       |
 | **os.path.isabs(path)**            | **判断是否为绝对路径**                                       |
 | **os.path.isfile(path)**           | **判断路径是否为文件**                                       |
 | **os.path.isdir(path)**            | **判断路径是否为目录**                                       |
 | **os.path.islink(path)**           | **判断路径是否为链接**                                       |
 | os.path.join(path1[,path2[,...]])  | 把目录和文件名合成一个路径                                   |
 | os.path.normcase(path)             | 转换path的大小写和斜杠                                       |
 | os.path.normpath(path)             | 规范path字符串形式                                           |
 | os.path.realpath(path)             | 返回path的真实路径                                           |
 | os.path.relpath(path[, start])     | 从start开始计算相对路径                                      |
 | os.path.samefile(path1, path2)     | 判断目录或文件是否相同                                       |
 | os.path.sameopenfile(fp1, fp2)     | 判断fp1和fp2是否指向同一文件                                 |
 | **os.path.split(path)**            | **把路径分割成 dirname 和 basename，返回一个元组**           |
 | **os.path.splitext(path)**         | **分割路径，返回路径名和文件扩展名的元组**                   |
 | **os.path.walk(path, visit, arg)** | **遍历path，进入每个目录都调用visit函数，visit函数必须有3个参数(arg, dirname, names)，dirname表示当前目录的目录名，names代表当前目录下的所有文件名，args则为walk的第三个参数** |

 ## JSON

 这是百度的说辞

 JSON（[JavaScript](https://baike.baidu.com/item/JavaScript?fromModule=lemma_inlink) Object Notation, JS对象简谱）是一种轻量级的数据交换格式。它基于 [ECMAScript](https://baike.baidu.com/item/ECMAScript?fromModule=lemma_inlink)（European Computer Manufacturers Association,  欧洲计算机协会制定的js规范）的一个子集，采用完全独立于编程语言的文本格式来存储和表示数据。简洁和清晰的层次结构使得 JSON  成为理想的数据交换语言。 易于人阅读和编写，同时也易于机器解析和生成，并有效地提升网络传输效率

 不要想的太复杂

 就把他理解成Python字典的变式

 Json是Python的一个内置库,所以无需安装，也是用户,软件配置数据存储较为**常用**的存储格式

 使用前先import json

 ### 转换

 1. **Json.loads**(Python字典)将Python的字典转化成Json格式
 2. **Json.dumps**将Json格式转化成Python字典格式

 ### 写读

 1. Json.load(fp)读取Json文件，fp为open(mode='r')
 2. Json.load(fp,Python字典)写入Json文件,fp为open(mode='w')

## 软件开发

通用软件开发框架

- electorn：基于node-js，跨平台，开发成本低，运行效率低
- qt：基于C++，跨平台，效率高，开发成本高
- javafx：基于java，主要用于跨平台桌面程序开发
- flutter：基于dart语言，谷歌开源移动UI框架，可以快速在iOS和Android上构建高质量的原生用户界面

通用Python开发框架

- PyQt：PyQt5是Qt v5的Python版本，功能强大复杂，提供QT Designer设计UI （GPL V3协议，开源，商用收费）
- Pyside: PySide2是来自QT for Python项目的官方Python模块 （LGPL协议，闭源商用）
- Tkinter：Python标准库，Tk GUI 工具包的接口 ，布局通过代码实现，简单易用，但开发效率低
- WxPython：开源免费，提供wxFormbuilder，压缩版PyQt

这里推荐PyQt5和Tkinter最大软件用**PyQt5**,做小软件使用**Tkinter**

PyQt5需要使用pip工具进行安装，而Tkinter是Python自带

在**cmd**运行此两行代码即可，也可以去找**作者**获得 *常见库安装脚本*

```shell
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pyqt5
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pyqt5-tools
```

PyQt5也可以进行可视化操作开发(直接往窗口上拖控件)，[Qt designer](https://build-system.fman.io/static/public/files/Qt%20Designer%20Setup.exe)是个QT自带的软件

Pycharm上的PyQt5开发

### PyCharm配置环境

启动PyCharm后，新建一个PyQt5空项目后，需要配置Qt Designer、pyuic、pyrcc工具，相关配置方法如下：

#### Qt Designer

Qt Designer 是通过拖拽的方式放置控件，并实时查看控件效果进行快速UI设计。

最终生成.ui文件（实质上是XML格式的文件），可以通过pyuic5工具转换成.py文件。

在Pycharm中，依次打开 File - Settings - Tools - External Tools，点击 + Create Tool，配置如下：

```
Name: QtDisigner

Program : C:\Python38\Lib\site-packages\pyqt5_tools\Qt\bin\designer.exe # 根据实际修改

Working directory: $FileDir$
```

![img](https://img2020.cnblogs.com/blog/445074/202003/445074-20200314115300752-1630379301.jpg)

#### PyUIC

PyUIC主要是把Qt Designer生成的.ui文件换成.py文件。

在Pycharm中，依次打开 File - Settings - Tools - External Tools，点击 + Create Tool，配置如下：

```
Name: PyUIC

Program : C:\Python\python.exe #根据实际修改

Arguments: -m PyQt5.uic.pyuic $FileName$ -o $FileNameWithoutExtension$.py

Working directory: $FileDir$
```

![img](https://img2020.cnblogs.com/blog/445074/202003/445074-20200314115331437-1598416503.jpg)

#### PyRCC配置

PyRCC主要是把编写的.qrc资源文件换成.py文件。

在Pycharm中，依次打开 File - Settings - Tools - External Tools，点击 + Create Tool，配置如下：

```
Name: PyRCC

Program : C:\Python\Scripts\pyrcc5.exe #根据实际修改

Arguments: $FileName$ -o $FileNameWithoutExtension$_rc.py

Working directory: $FileDir$
```

![img](https://img2020.cnblogs.com/blog/445074/202003/445074-20200314115348431-79535743.jpg)

*图片来自[lovesoo - 博客园 (cnblogs.com)](https://www.cnblogs.com/lovesoo/)

### 第一个窗口

这里给出一段Demo 程序,利用PyQt创建了一个窗口

![image-20230111173055485](https://599575461.github.io/Teaching/img/image-20230111173055485.png)

如果看不懂，我们逐一分析

```python
# 导入sys库
import sys
# 导入PyQt5中的QtWidgets
from PyQt5 import QtWidgets

# 定义Main类，继承QtWidgets.QMainWindow
class Main(QtWidgets.QMainWindow):
    def __init__(self):
        # 定义超类，兼容Python2
        super(Main, self).__init__()


if __name__ == '__main__':
    # 定义app为QtWidgets.QApplication的实例化，把外部参数传进去
    app = QtWidgets.QApplication(sys.argv)
    # 实例化Mian一个窗口
    main = Main()
    # 让这个窗口显示
    main.show()
    # 循环刷新，当退出时调用sys.exit退出
    sys.exit(app.exec_())
```

运行这段就会出现一个窗口

![image-20230111173646919](https://599575461.github.io/Teaching/img/image-20230111173646919.png)

但是现在这个窗口是白的什么都没有，我们需要设置他的**标题，图标，内容**等

```python
import sys

from PyQt5 import QtWidgets


class Main(QtWidgets.QMainWindow):
    def __init__(self):
        super(Main, self).__init__()
        # 设置窗口标题为Demo
        self.setWindowTitle('Demo')
        # 设置长宽
        self.resize(800, 430)


if __name__ == '__main__':
    app = QtWidgets.QApplication(sys.argv)
    main = Main()
    main.show()
    sys.exit(app.exec_())

```

现在在super下面设置窗口标题

使用**self.setWindowTitle**方法

setWindowTitle直译过来就是*设置窗口标题*

想要改变窗口大小使用**self.resize**方法，这里设置长：800，宽：430

运行后的效果：

![image-20230111174504529](https://599575461.github.io/Teaching/img/image-20230111174504529.png)







