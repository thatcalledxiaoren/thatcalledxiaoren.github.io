![logo](/logo.jpg)
##[首页](/) [小鸡吃沙威玛](/ces/index.html) [实用工具](/tool/index.html) [文档](/doc/index.html) [联系](mailto:lihaoqian12@outlook.com)
#文档#A102 关键字
[TOC]
##概述
关键字指C++自带的类型，函数，以及一些*iaefgvuagdhnufasnhiiiiidaf*。
这里提到个关键字只是一小部分，还有很多，这里不一一阐述。
##类型
|类型|范围（正负）|字节|精度|
|-------------|--------------|----|-------|
| int         | 2^31^        | 4  | 0     |
| long        | 2^31^        | 4  | 0     |
| long long   | 2^63^        | 8  | 0     |
| float       | ==约==3.4*10^38^   | 4  | 7     |
| double      | ==约==1.8*10^308^  | 8  | 15    |
| long double | ==约==1.1*10^4932^ | 16 | 18~21 |
| bool        | 1            | 1  | 0     |
| char        | 128          | 2  | 0     |
`unsigned X`:无标识符。如`unsigned char`的范围是0~256(128*2).
`signed`:有标识符。==必要时可以替代int。==
`const`:无法被修改。如`const int pi=3.14;`定义了一个叫做pi的实数，其值无法被修改。==但一般使用[#define](/doc/A103)来替代。==
`auto`:让程序自己决定用哪个。
##函数
###for
```cpp
for(A;B;C){}
```
**A**:计数器。形如`int i=0`，定义了一个从0开始的计数器。
**B**:运行条件。形如`i<n`，表示当i<n时运行for循环。
**C**:步长。形如`i++`，表示每执行一次循坏运行一次i++。
####另外一种用法
```cpp
for(A:B){}
```
**A**:迭代器。一般使用`auto i`，代表一个名字叫i的迭代器。对于一个int类型的vector,可以使用`vector<int>::iterator`（很明显比auto长）。
**B**:容器。很简单，定义的名字叫什么就用什么。
==需要注意的是，这种方法只适用于STL容器，而且只有C++ 11及以上才拥有这种使用方法。==对于C++ 99，可使用:
```cpp
for(auto i=v.begin();i<v.end();i++){}
```
###while
```cpp
while(A){}
```
很简单。如果A，执行代码，直到!A。
###do-while
```cpp
do{}while(A)
```
与while不同，先执行代码，再判断，直到!A。
###if大家族
```cpp
if(A){a}
else if(B){b}
else{c}
```
如果A,执行a，如果B,执行b，否则执行c。==a,b,c合计只执行一次。==
###switch
```cpp
switch(n){
	case a:
    	//1
    case b:
    	//2
    default:
    	//3
}
```
如果n=a,执行1。如果n=b,执行2。默认执行3。
==但执行完一条语句后，switch还会继续往下搜索。==如果想要只执行一次，在语句后加上`break;`。
***CASE,DEFAULT后面加的是冒号！！！***
###break,continue
在循环体中，break代表跳出循环体，continue代表略过以下的代码。
#终于写完了！！！