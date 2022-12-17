# Python

 ## 变量

> 格式: 变量名=数据
>
> ```python
> a=1
> #定义了一个a的变量
> b=1
> #定义了一个b的变量
> 
> #以上变量都为int类型
> ```
>
> 以上例子的数据类型为整数(整型)
>
> ```python
> a="我是Installation"
> #定义了一个文本类型变量(字符串)
> ```
>
> |  数据类型  | 对应关键字                       |
> | :--------: | -------------------------------- |
> |  文本类型  | `str`                            |
> |  数值类型  | `int` `float` `complex`          |
> |  序列类型  | `list` `tuple` `range`           |
> |  映射类型  | `dict`                           |
> |  集合类型  | `set` `frozenset`                |
> |  布尔类型  | `bool`                           |
> | 二进制类型 | `bytes` `bytearray` `memoryview` |
>
> 记住关键的**int整型,str字符型**

## 函数

> 前面讲到程序就是**数据**和**函数**,调用函数修改数据就是编程本质
>
> 函数可以理解为一个**方法**(在类里面就叫做方法,在类外才叫做函数),里面放一些代码,可以被重复调用
>
> 调用函数是会执行函数里面的代码
>
> 创建函数格式:def 函数名(参数):
>
> 1. 参数可以不填,尤其记住后面要有一个**冒号**
> 2. 标点符号必须是英文
> 3. 写在函数体里面的代码前面必须有缩进(一个Tab的长度)
>
> 调用格式:函数名(参数)
>
> 1. 与创建函数一样标点符号必须是英文
> 2. 调用函数时不用在前面加缩进
>
> ```python
> def helloworld():
>     #定义一个函数,作用是打印Hello World
>     print("Hello World")
> #调用这个函数
> helloworld()
> 
> >>>Hello World
> ```
>
> - ## 参数
>
>   在调用函数时，通常会传递参数，函数内部的代码保持不变，针对 **不同的参数 处理 不同的数据**。
>
>   有位置传参、关键字传参、默认值参数、多值参数等
>
>   - **形参**：**定义** 函数时的 参数变量
>   - **实参**：**调用** 函数时，使用的参数变量
>
>   参数传递的过程，就是 把实参的引用 传递给 形参 ，使用实参的值来执行函数体的过程。
>
>   在 `Python` 中，函数的 **实参**/**返回值** 都是是靠 **引用** 来传递来的
>
>   ### 1 . 位置实参
>
>   按照参数位置，依次传递参数，这是最普通的方式
>
>   ```python
>   def sum(a, b)
>       print(a + b)
>                   
>   sum(3, 9)
>   #调用函数时，按顺序传递参数，3 传给 a，9 传给 b
>                   
>   >>>12
>   ```
>
>   ### 2 . 如果不想按照顺序传递参数，也可以按关键字传递,效果一样
>
>   ```python
>   def sum(a, b)
>       print(a + b)
>                   
>   sum(b = 3, a = 9)
>   #调用函数时，按关键字传递参数，3 传给 b，9 传给 a
>                   
>   >>>12
>   ```
>
>   以上两种最常见,其余后文会说到
>
>   - ## 返回值
>
>     > 在函数体内写return关键字,后面写返回内容
>     >
>     > 格式: return 返回内容
>     >
>     > - 返回的内容可以是任何数据类型
>     > - 返回的内容可以是函数(装饰器会讲)
>     > - 写了返回后return后面的代码不会执行
>     >
>     > ```python
>     > def sum(a, b)
>     >     return a+b
>     > 
>     > print(location(3,9))
>     > #调用函数时传入参数,然后返回a+b
>     > 
>     > >>>12
>     > ```
>     >
>     > ```python
>     > def booltest()
>     >     return True
>     > 
>     > print(booltest())
>     > #返回值也可以是bool类型
>     > 
>     > >>>True
>     > ```

## 开发工具

> - ## PyCharm
>
>   PyCharm是一种[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink) [IDE](https://baike.baidu.com/item/IDE/8232086?fromModule=lemma_inlink)（Integrated Development Environment，集成开发环境），带有一整套可以帮助用户在使用[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink)语言开发时提高其效率的工具，比如[调试](https://baike.baidu.com/item/调试/5852756?fromModule=lemma_inlink)、[语法高亮](https://baike.baidu.com/item/语法高亮/9686751?fromModule=lemma_inlink)、[项目管理](https://baike.baidu.com/item/项目管理/85389?fromModule=lemma_inlink)、代码跳转、智能提示、[自动完成](https://baike.baidu.com/item/自动完成/22748028?fromModule=lemma_inlink)、[单元测试](https://baike.baidu.com/item/单元测试/1917084?fromModule=lemma_inlink)、[版本控制](https://baike.baidu.com/item/版本控制/3311252?fromModule=lemma_inlink)。此外，该IDE提供了一些高级功能，以用于支持[Django](https://baike.baidu.com/item/Django/61531?fromModule=lemma_inlink)框架下的专业[Web](https://baike.baidu.com/item/Web/150564?fromModule=lemma_inlink)开发
>
> 
>
>   PyCharm是最受Python程序员喜爱的Python编辑器,本人**推荐使用这个**
>
>   但是专业版收费,具体信息去[官网](https://www.jetbrains.com/pycharm/)查看
>
> - ## Visual Studio Code
>
>   Visual Studio Code（简称“VS Code”）是Microsoft在2015年4月30日[Build](https://baike.baidu.com/item/Build/15992854?fromModule=lemma_inlink)开发者大会上正式宣布一个运行于 [MacOS](https://baike.baidu.com/item/Mac OS X/470629?fromModule=lemma_inlink)、[Windows](https://baike.baidu.com/item/Windows?fromModule=lemma_inlink)和[ Linux](https://baike.baidu.com/item/ Linux/27050?fromModule=lemma_inlink) 之上的，针对于编写现代[Web](https://baike.baidu.com/item/Web/150564?fromModule=lemma_inlink)和[云应用](https://baike.baidu.com/item/云应用/476249?fromModule=lemma_inlink)的跨平台[源代码编辑器](https://baike.baidu.com/item/源代码编辑器/16273015?fromModule=lemma_inlink)可在桌面上运行，并且可用于[Windows](https://baike.baidu.com/item/Windows/165458?fromModule=lemma_inlink)，[macOS](https://baike.baidu.com/item/macOS/8654551?fromModule=lemma_inlink)和[Linux](https://baike.baidu.com/item/Linux/27050?fromModule=lemma_inlink)
>
>   它具有对[JavaScript](https://baike.baidu.com/item/JavaScript/321142?fromModule=lemma_inlink)，[TypeScript](https://baike.baidu.com/item/TypeScript/4314718?fromModule=lemma_inlink)和[Node.js](https://baike.baidu.com/item/Node.js/7567977?fromModule=lemma_inlink)的内置支持，并具有丰富的其他语言（例如[C++](https://baike.baidu.com/item/C%2B%2B/99272?fromModule=lemma_inlink)，[C＃](https://baike.baidu.com/item/C＃/195147?fromModule=lemma_inlink)，[Java](https://baike.baidu.com/item/Java/85979?fromModule=lemma_inlink)，[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink)，[PHP](https://baike.baidu.com/item/PHP/9337?fromModule=lemma_inlink)，[Go](https://baike.baidu.com/item/Go/953521?fromModule=lemma_inlink)）和运行时（例如[.NET](https://baike.baidu.com/item/.NET/156737?fromModule=lemma_inlink)和[Unity](https://baike.baidu.com/item/Unity/10793?fromModule=lemma_inlink)）扩展的[生态系统](https://baike.baidu.com/item/生态系统/457895?fromModule=lemma_inlink)
>
> 
>
>   Visual Studio Code几乎可以写**任何编程语言**,当然用来写Python也是不错的
>
>   它的体积比PyCharm小,但是Visual Studio Code终究还是一个编辑器,无法与IDE相提并论
>
>   具体信息去[官网](https://code.visualstudio.com/)查看
>
> - ## Sublime Text
>
>   Sublime Text 是一个文本[编辑器](https://baike.baidu.com/item/编辑器/9067697?fromModule=lemma_inlink)（收费[软件](https://baike.baidu.com/item/软件/12053?fromModule=lemma_inlink)，可以无限期试用），同时也是一个先进的[代码](https://baike.baidu.com/item/代码/86048?fromModule=lemma_inlink)编辑器。Sublime Text是由程序员Jon Skinner于2008年1月份所开发出来，它最初被设计为一个具有丰富扩展功能的[Vim](https://baike.baidu.com/item/Vim?fromModule=lemma_inlink)
>
>   Sublime Text具有漂亮的用户界面和强大的功能，例如代码缩略图，[Python](https://baike.baidu.com/item/Python?fromModule=lemma_inlink)的插件，代码段等。还可自定义键绑定，菜单和工具栏。Sublime Text 的主要功能包括：拼写检查，书签，完整的 [Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink) API, 即时项目切换，多选择，多窗口等等。[Sublime](https://baike.baidu.com/item/Sublime/8130415?fromModule=lemma_inlink) Text 是一个跨平台的编辑器，同时支持Windows、[Linux](https://baike.baidu.com/item/Linux?fromModule=lemma_inlink)、[MacOS](https://baike.baidu.com/item/Mac OS X?fromModule=lemma_inlink)等操作系统
>
> 
>
>   这是一款不错的Python开发工具,但与前两者相比个人感觉比不上
>
>   具体信息去[官网](https://www.sublimetext.com/)查看
>
> 具体使用哪个看个人需求,另外安装了工具还要装Python解释器
>
> - ## Python安装
>
>   下表复制Python官网**3.9.2**安装列表根据需求进行下载
>
>   一般如果你是Windows操作系统直接点最后一个
>
>   |                             版本                             | 操作系统 |
>   | :----------------------------------------------------------: | :------: |
>   | [压缩源码包](https://www.python.org/ftp/python/3.9.2/Python-3.9.2.tgz) |   源码   |
>   | [XZ 压缩源压缩包](https://www.python.org/ftp/python/3.9.2/Python-3.9.2.tar.xz) |   源码   |
>   | [macOS 64 位英特尔安装程序](https://www.python.org/ftp/python/3.9.2/python-3.9.2-macosx10.9.pkg) |   Mac    |
>   | [macOS 64 位通用2 安装程序](https://www.python.org/ftp/python/3.9.2/python-3.9.2-macos11.pkg) |   Mac    |
>   | [Windows 嵌入式程序包（32 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2-embed-win32.zip) | Windows  |
>   | [Windows 嵌入式程序包（64 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2-embed-amd64.zip) | Windows  |
>   | [Windows帮助文件](https://www.python.org/ftp/python/3.9.2/python392.chm) | Windows  |
>   | [Windows安装程序（32 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2.exe) | Windows  |
>   | [Windows安装程序（64 位）](https://www.python.org/ftp/python/3.9.2/python-3.9.2-amd64.exe) | Windows  |
>
>   **双击安装包随后按照步骤来安装(照片是3.10.8的安装,给出的链接是3.9.2的,步骤都一样)**
>
> <img src=".\img\Install_python.png" alt="Install_python" style="zoom:80%;" /> 
>
> 等待安装成功,看见**Successfully**表示成功安装

## 面向对象

> **面向对象是高级编程语言的重点**
>
> 面向对象程序设计以对象为核心，该方法认为程序由一系列对象组成
>
> 类是对现实世界的抽象，包括表示静态属性的数据和对数据的操作，对象是类的实例化。 对象间通过消息传递相互通信，来模拟现实世界中不同实体间的联系。 在面向对象的程序设计中，对象是组成程序的基本模块
>
> 通俗点就是**变量和函数的整合**
>
> 面向对象三大基本特征：**封装、继承、多态**(这些以后会讲)
>
> 而面向对象的过程就是找对象、建立对象、使用对象、维护对象的关系的过程
>
> 格式:class 类名(继承的类):
>
> 继承后面会学,继承的类可以不填
>
> 写在类里面的函数的第一个参数是self(顾名思义,就是自己的意思)
>
> ```python
> class Test():
>     #创建一个类
>     def __init__(self):
>       	pass
> 
>     #创建一个在类里面的函数(方法)
>     def printhello(self):
>       	print("hello world")
> #实列化对象
> p=Tes()
> #执行类里面的函数
> p.printhello()
> ```
> 
>在类中定义\_\_init\_\_函数(构造函数),在执行p=People()是会执行\_\_init\_\_函数里的代码(实列化对象)

