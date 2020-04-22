Class
=====
这个东西真的很神奇
--------------
> 基本类
~~~
class box{
public:
    void box();                 //构造函数（与class同名）
    void box(const box& obj);   //析构函数（快速复制对象）
    void ~box();                //对象被删除时调用
    void box(...);              //构造函数 box()的重载函数
    double operator+(...);      //这个相当厉害，可以自定义类的运算符
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
