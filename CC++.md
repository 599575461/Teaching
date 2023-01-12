# C/C++

## 变量

C和C++属于**强类型**语言,不同于Python的是他们在定义变量时必须指定变量**数据类型**

格式:数据类型 变量名=数据

这也是**大多数语言**所采取的定义变量格式

C++:

```c++
int a = 1 //定义变量a为1
```

C:

```c
int a = 1 //定义变量a为1,与C++的语法一样
```

上面的列子程序不会**直接执行**

在C/C++中程序开始执行时是执行**main函数**里面的内容

至于函数是啥去看Python里的函数概念`

C/C++数据类型

| 类型     | 关键字  |
| :------- | :------ |
| 布尔型   | bool    |
| 字符型   | char    |
| 整型     | int     |
| 浮点型   | float   |
| 双浮点型 | double  |
| 无类型   | void    |
| 宽字符型 | wchar_t |

NULL为空类型,也就是什么都没有

在C++中引入了string类型让字符变得更加容易操作

## 函数

在C/C++中定义函数

格式为:函数类型 函数名(参数){}

```C++
int a(){ //定义一个函数
    int b=1;//函数内容为定义b为1
}
```

### 主函数

前面说到C/C++中程序开始执行时是执行**main函数**里面的内容

那么我们先定义main函数

```c++
int main(){//定义一个主函数
    int a=1;//函数内容为定义b为1
}
```

### 输出

在C++中输出需要用到iostream

在C中输出需要用到studio.h

C++:

```c++
#include <iostream>

int main(){
    std::cout<<"Hello world"<<std::endl;//std::endl表示换行
    //使用std::cout进行打印
}

```

C:

```C
#include <studio.h>

int main(){
    //使用printf进行打印
    printf("Hello world\n")
}
```











