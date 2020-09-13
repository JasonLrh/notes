## undefined reference to `__errno'
nano.specs缺少了很多东西
~~~
-lg  ...  -specs=rdimon.specs  -specs=nosys.specs
~~~

## 莫名其妙进入 Infinite_Loop (位于startup_xxx.s)

> 其实是进入了未定义的中断函数  
> 调试的时候调用堆栈会显示从WWDG_IRQHandler等产生  
> > 需要在xxx_it.c/.h中添加中断函数，并建立回调

