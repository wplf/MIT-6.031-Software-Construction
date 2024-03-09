# 11-Abstraction Functions & Rep Invariants



## 不变量： 

- 在该作用范围下，一定为True的条件或常量
- 错误示范： 在某些情况下，如果将变量的指针暴露出去， 它就变成了可变量。
- 对于可变类型来说，可以使用 不可变的 wrapper 包装

## 抽象函数

- 抽象函数 定义： 将表示值 映射到他们表示的 抽象值上的函数

图中的映射即为抽象函数

![](D:\00-self-study\mit-6.031-Software_Construction\images\11-abstract function.png)

- 表示不变量定义： 将 表示值映射到 boolean 中的函数



## beneficent mutation

- 只修改函数内部的表示value， 但是还会映射到同一个抽象值中。





## 设计 ADT， 抽象数据类型需要考虑

- two spaces

  1.  抽象值域： for specs

  2. 表示值域： for implementation

- 表示值域 在什么范围是合法的

- 表示值域 如何映射到 抽象值域



## Summary

- 不变量是 ADT 实例 永远为 true 的属性
- 好的ADT 有自己的不变量，  必须由  creators and producers 创建，由 observers and mutators 管理
- 表示不变量 确定了 表示的合法空间， 并且需要每次都被 check
-  abstraction function 将表示值域映射到值域
- 表示域暴露是非常不好的
- 不变量应该做好 document， 而且需要被 assertion。