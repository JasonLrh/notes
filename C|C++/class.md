Class
=====
> 前言：class(类)是C++相对C特有的、处理面向对象思想的字段。不过俺觉得，C99往后的struct基本上来说可以替代大部分的class操作，为啥要整个class出来呢？

> 结果看到operator的时候豁然开朗——噫，高级。

这个东西真的很神奇
--------------
> 基本类
~~~
class box{
public:
    void box();                 //构造函数（与class同名）
    void box(const box& obj);   //拷贝构造函数（快速复制对象）
    void ~box();                //析构函数，对象被删除时调用
    void box(...);              //构造函数 box()的重载函数
    double operator+(...);      //运算重载函数。这个相当厉害，可以自定义类的运算符
    double operator+(....);     //运算重载函数的重载函数
    ...
protect:
    ...
private:
    static int countor;
    ...
}
~~~
静态变量必须在外部初始化，这个变量在所有的同类中是同一个对象
~~~
int box::countor = 0;
~~~
> 封装类(public继承)
~~~
class Box::public box{
    ...
}
~~~
