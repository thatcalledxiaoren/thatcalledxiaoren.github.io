![logo](/logo.jpg)
##[首页](/) [小鸡吃沙威玛](/ces/index.html) [实用工具](/tool/index.html) [文档](/doc/index.html) [联系](mailto:lihaoqian12@outlook.com)
#文档#A103 系统函数
[TOC]
##\#类
###\#include
```cpp
#include <filename>
//或
#include "filename"
```
引用名叫filename的文件。尖括号与双引号的不同在于，尖括号是在编译器文件夹里引用，而双引号则是在文件所在文件夹中引用。
###\#define
```cpp
#define a b
```
将a定义为b。注意，这里的==定义==指编译器在发现与a相同的正则表达式时，看作是b。因此，我们可以玩一些……
####骚操作
```cpp
#define int long long
```
再也不用开long long!不过，你编译的时候，可能会看到：
`cc1plus.exe [错误] '::main' must return 'int'`
main函数必须返回int!怎么办？还记得我们在[这里](/doc/A102)提到的signed吗？此时，我们就可以……
```cpp
signed main(){}
```
了！
###\#pragma
很少用到。不过，可以用于优化代码和输出：
####Optimize优化
```cpp
#pragma GCC optimize(x)
```
O1优化会消耗少得多的编译时间，它主要对代码的分支，常量以及表达式等进行优化。
O2会尝试更多的寄存器级的优化以及指令级的优化，它会在编译期间占用更多的内存和编译时间。
O3在O2的基础上进行更多的优化，例如使用伪寄存器网络，普通函数的内联，以及针对循环的更多优化。
还不满足？试试文章最后的大火车!!
####输出
```cpp
#pragma message(str)
```
输出str。不过没人这么干。
###\#if大家族
常用的一般是#ifdef/ifndef。
```cpp
#ifdef __cplusplus
//1
#else
//2
#endif
```
如果定义__cplusplus，执行1。否则，执行2。相反地，#ifndef指如果没有定义。
***一定要写#endif !!!***
千万不要在函数里面用这类if,你会***死得很惨***。
##饿啊啊我不要再写了
##大火车
```cpp
#pragma GCC target("avx")
#pragma GCC optimize(3)
#pragma GCC optimize("Ofast")
#pragma GCC optimize("inline")
#pragma GCC optimize("-fgcse")
#pragma GCC optimize("-fgcse-lm")
#pragma GCC optimize("-fipa-sra")
#pragma GCC optimize("-ftree-pre")
#pragma GCC optimize("-ftree-vrp")
#pragma GCC optimize("-fpeephole2")
#pragma GCC optimize("-ffast-math")
#pragma GCC optimize("-fsched-spec")
#pragma GCC optimize("unroll-loops")
#pragma GCC optimize("-falign-jumps")
#pragma GCC optimize("-falign-loops")
#pragma GCC optimize("-falign-labels")
#pragma GCC optimize("-fdevirtualize")
#pragma GCC optimize("-fcaller-saves")
#pragma GCC optimize("-fcrossjumping")
#pragma GCC optimize("-fthread-jumps")
#pragma GCC optimize("-funroll-loops")
#pragma GCC optimize("-fwhole-program")
#pragma GCC optimize("-freorder-blocks")
#pragma GCC optimize("-fschedule-insns")
#pragma GCC optimize("inline-functions")
#pragma GCC optimize("-ftree-tail-merge")
#pragma GCC optimize("-fschedule-insns2")
#pragma GCC optimize("-fstrict-aliasing")
#pragma GCC optimize("-fstrict-overflow")
#pragma GCC optimize("-falign-functions")
#pragma GCC optimize("-fcse-skip-blocks")
#pragma GCC optimize("-fcse-follow-jumps")
#pragma GCC optimize("-fsched-interblock")
#pragma GCC optimize("-fpartial-inlining")
#pragma GCC optimize("no-stack-protector")
#pragma GCC optimize("-freorder-functions")
#pragma GCC optimize("-findirect-inlining")
#pragma GCC optimize("-fhoist-adjacent-loads")
#pragma GCC optimize("-frerun-cse-after-loop")
#pragma GCC optimize("inline-small-functions")
#pragma GCC optimize("-finline-small-functions")
#pragma GCC optimize("-ftree-switch-conversion")
#pragma GCC optimize("-foptimize-sibling-calls")
#pragma GCC optimize("-fexpensive-optimizations")
#pragma GCC optimize("-funsafe-loop-optimizations")
#pragma GCC optimize("inline-functions-called-once")
#pragma GCC optimize("-fdelete-null-pointer-checks")

```