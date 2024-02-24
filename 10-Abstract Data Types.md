# 10-Abstract Data Types



名词解释 

- 抽象
- 模块化
- 封装
- 信息隐藏
- concern separation



在写某些方法时， 最好情况是：

- 抽象， 只看 precondition 和 postcondition 就可以了解函数，不用去看具体实现
- modularity， 每个木块自己做测试
- 封装， 局部变量只由内部去修改
- 信息隐藏
- separation of concerns



## Classifying types and operations

对某些定义好的类型，可变类型，他的操作可分为以下几类

1.  创造， 创造新实例
2.  producer， 使用多个实例生成新的实例

3. 观察， 返回实例属性
4. mutator， 修改实例属性。

## An abstract type is defined by its operations

![](D:\00-self-study\mit-6.031-Software_Construction\images\10-abstract-type.png)

## 总结

- 抽象数据类型由其操作表征
- 操作可以分为  creators, producers, observers, and mutators.
- 一个 ADT 是他们操作和 specs 的集合
- 好的 ADT 应该 简单、一致、充足，且不依赖于其他任何东西
- 一个 ADT 应该在test时， 应该对一组case 测试所有操作。