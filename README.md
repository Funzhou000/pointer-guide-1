# pointer-guide-1
# pointer

指针的长度8bit，64位操作系统&#x20;

## 1.指针基本概念

\*两种含义{1-前面有类型，后面的变量是指针&#x20;

2-使用时：表示取值；（取指针内存里的值）}

int a；

\&a取得是最前面的地址（a整型占四个字节，有四个地址）；

&取的地址都是最前面的地址（&补充）

int*与char*\*区别：步长不一样；

eg：

cout<\<p(p为整型指针)；cout<\<q(q is char pointer);

cout<\<p+!; cout<\<q+1;

整型指针地址间隔4，char 指针间隔1；

reason：指针+1是让读取下一个整型/像一个字符；一个整型占四个字节，一个char占1个字节，所以地址间隔不一样

//字符占一个字节

## 2.指针应用

```c
void swap (int x,int y)
{ int t=a;
a=b;
b=t;}
int main {
swap（a,b);//如果要交换实参的值必须要传递地址
printf("%d,%d",a,b)
return 0 ;
}
//修改后
void swap (int *x,int *y)
{ int t=*a;
*a=*b;
*b=t;}
int main {
swap（&a,&b);//如果要交换实参的值必须要传递地址
printf("%d,%d",a,b)
return 0 ;
}
```

实际上并不会交换数字；

reason：函数执行完最后一步要释放占空间。x，y被释放掉

补充：什么是形参什么是实参

形参是函数定义时的参数，它们就像是函数的占位符，等到函数调用时再具体化。实参则是函数调用时实际传递给函数的值或变量。也就是说，形参是你写函数时用来接收数据的，实参是你调用函数时实际传递的数据

## 3.指针的运算

*\*px++++与(\*++*++px)++有区别；++

练习（实现下库函数）



> 快速介绍下stringcopy{
>
> `strcpy` 是 C 语言中的一个函数，用于将一个字符串复制到另一个字符串。它的基本用法是 `strcpy(destination, source)`，其中 `source` 是要复制的字符串，而 `destination` 是目标字符串。`strcpy` 会从源字符串的起始位置开始，逐个字符复制到目标字符串，直到遇到 `\0`（字符串结束标志）。需要注意的是，目标字符串必须有足够的空间来容纳源字符串及其终止}

实现strcpy（stringcopy）

