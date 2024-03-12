# Recursive data type

递归的数据类型， 课程中以递归的 不可变list举例， 定义了抽象数据类型 Imlist



| empty: void → ImList      | // returns an empty list                                     |
| :------------------------ | ------------------------------------------------------------ |
| cons: E × ImList → ImList | // returns a new list formed by adding an element to the front of another list |
| first: ImList → E         | // returns the first element of a list, requires the list to be nonempty |
| rest: ImList → ImList     | // returns the list of all elements of this list except for the first, requires the list to be nonempty |



Imlist 的数据接口如下

```Java
public interface ImList<E> {
    // todo: empty() returning ImList<E>
    public ImList<E> cons(E elt);
    public E first();
    public ImList<E> rest();
}
```



注意，本文花了大篇幅讲解 static 方法该怎么使用， 如果该方法不应该被任意一个实例绑定，那么他应该被设置为类方法。

例如 下列接口中的 Empty

```java
public interface ImList<E> {
    public static <E> ImList<E> empty() {
        return new Empty<>();
    }
    public ImList<E> cons(E elt);
    public E first();
    public ImList<E> rest();
}
```



这种递归数据类型的典型例子是 链表 和 tree， 如果拿到根节点，非常容易实现并行。

