# 12-Interfaces, Generics, Enums, and Functions



## Interface

java 的 interface 是抽象数据类型的典型， interface 是一系列没有函数 body， 只有签名的方法， 他不能创建实例， 给其他的类型提供了通用的接口。

例如 List 是接口， ArrayList 是实例类， 其必须满足所有 List 提供的接口才能通过编译器检查。

`new ArrayList<String> `  合法，`new List<String>` 不合法

## Subtypes

子类型可以通过 接口 实现， 也可以通过 继承 实现

```java
class ArrayList<E> implements List<E> {
    ...
}

interface SortedSet<E> extends Set<E> {
    ...
}
```

复习概念， 抽象方法， abstraction function 是建立 从 rep 到 abstract 的映射，

### 通用设计逻辑

1.  抽象方法应该被记录
2. 表示不变量应该被记录
3. rep field 应该是final
4. 构造方法应该是 private， 创建 obj 时通过 creator 函数， 或者 mutator 创造

### 为什么用 interface

1. 对编译器和human来说都更易理解
2. 允许多种不同性能的实现， 例如 ArrayList 和 LinkedList 实现
3. 给 spec 留出了更多的空间
4. 给同一个类可能提供了多种视角
5. 实现更 more or less trustworthy 

## Subclassing

子类与实现接口 都会实现同样的方法， 子类可以覆盖父类的方法body，而且 其spec约束的作用可能会更强。

1. 子类继承了父类所有的实例方法， 包含method body等， 也可以重写
2. 子类继承了父类的 field，即 rep
3. 子类能创建新的实例方法



子类继承父类的 rep 可能会带来以下缺点

1. rep 暴露在所有的 父类和子类
2.  父类和子类的 rep 中存在依赖关系
3. 父类可能会不经意修改子类的 rep



## 泛型 （generic）

泛型的 interface 举例

``` java
public interface Set<E> {

    // ...

    /**
     * Test for membership.
     * @param e an element
     * @return true iff this set contains e
     */
    public boolean contains(E e);

    /**
     * Modifies this set by adding e to the set.
     * @param e element to add
     */
    public void add(E e);

    // ...
}

```

```java

public class CharSet implements Set<Character> {

    private String s = "";
    // ...

    @Override
    public boolean contains(Character e) {
        checkRep();
        return s.indexOf(e) != -1;
    }

    @Override
    public void add(Character e) {
        if (!contains(e)) s += e;
        checkRep();
    }
    // ...
}
```

## 枚举类型



## ADT in java

![](D:\00-self-study\mit-6.031-Software_Construction\images\12-interface-generics-enums.png)
