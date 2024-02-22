# 04-Code review



## code format

```java
if (isOdd(n)) {
    n = 3*n + 1;
}
```

## comments format

```java
/**
 * Compute the hailstone sequence.
 * See http://en.wikipedia.org/wiki/Collatz_conjecture#Statement_of_the_problem
 * @param n starting number of sequence; requires n > 0.
 * @return the hailstone sequence starting at n and ending with 1.
 *         For example, hailstone(3)=[3,10,5,16,8,4,2,1].
 */
public static List<Integer> hailstoneSequence(int n) {
    ...
}
```



## Avoid magic numbers 

使用变量

## 变量名规范

对于类来说，第一个字母大写

`python`： 使用下划线，蛇形命名

`java`： 使用`camelCase` 驼峰命名

[命名规范]([Effectively Naming Software Thingies | by Sagi Rabinovich | Medium](https://medium.com/@rabinovichsagi/effectively-naming-software-thingies-fcea9d78a699))

- 选择表意清晰的命名
- 变量名间要有区分度
- 使用上下文帮忙区分：   `address.state` or `engine.state`
- 使用解决方案领域的命名
- 使用问题领域的命名 
- 不要简写
- **变量名可读**
- 丢掉协议
- 不要使用双冠
- 对于常用的操作，遵循惯例

## 不要使用全局**变量**， 可以用常量



## 变量的类型

1. 局部变量
2. 实例变量： 
   1. `java： field`
   2. `JS：property`
   3. `member variable： C++`
   4. `attribute： python`
3. 静态变量： 和类绑定

## 方法应该返回结果，而不是打印结果

## 如果代码可以不处理特殊情况，则不用特殊处理