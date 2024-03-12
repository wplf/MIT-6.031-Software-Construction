# Equality 

Equality 是实现 ADT 的必要手段， 其保证了 ADT 的唯一性， 也保证了 ADT 的正确性。

Abstract function 是定义不可变数据类型的基础， 我们必须重写 equals 和 hashCode 方法， 以保证数据的唯一性。

## == vs. equals
||reference equality| object equality|
|---|---|---|
|java|==|equals|
|C#|==|Equals|
|python|is=|==|

## 定义equality
- observational equality: 当前观察的情况下是相同的，不代表以后观察还是相同。
- behavioral equality： 当前观察的情况相同，假如以后有修改，以后的情况也有相同。 

可以理解为引用传递和值传递。

1. 可变类型的 equality， 
对于python的list， 其相等满足observational equality， 但是不满足behavioral equality。


2. 不可变类型的 equality， 满足observational equality 和 behavioral equality


## final rules for equals() and hashCode()

for mutable objects:
1. 