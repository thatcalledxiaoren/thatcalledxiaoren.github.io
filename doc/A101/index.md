![logo](/logo.jpg)
##[首页](/) [小鸡吃沙威玛](/ces/index.html) [实用工具](/tool/index.html) [文档](/doc/index.html) [联系](mailto:lihaoqian12@outlook.com)
#文档#A101 代码模板
[TOC]
```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
	cout<<"Hello world!"<<endl;
    return 0;
}
```
##逐行分析
###1.
```cpp
#include<bits/stdc++.h>
```
引用bits文件夹下属的stdc++.h头文件。这个文件概括了你所需要的几乎一切库。对于输入输出，我们应引用：
```cpp
#include<iostream>
```
###2.
```cpp
using namespace std;
```
使用命名空间std(standard)。这行代码可以节省你不少时间（见下文）。
###3.和6.
```cpp
int main(){
	//...
}
```
定义main函数。与Python不同，C++在定义函数时需要提供函数返回值，int则代表整数。==如果不是int，会报错。==程序默认先运行main函数。
###4.
```cpp
cout<<"Hello world!"<<endl;
```
cout是输出流。它会输出`<<`后的内容。数个内容由`<<`链接。endl是换行符。
此外，`cout`和`endl`都定义在std命名空间。如果不写第二行，此行应写作：

```cpp
std::cout<<"Hello world!"<<std::endl;
```
###5.
```cpp
return 0;
```
返回0。返回0代表你的程序成功运行并正常结束。相反地，如果返回类似于1,3,3221225477这类奇怪的数，证明你的程序出问题了。
###最后一次更新:2025/5/19