# Reading 2: Basic Java

##  Software in 6.031

| Safe from bugs                                   | Easy to understand                                           | Ready for change                                  |
| :----------------------------------------------- | :----------------------------------------------------------- | :------------------------------------------------ |
| Correct today and correct in the unknown future. | Communicating clearly with future programmers, including future you. | Designed to accommodate change without rewriting. |



## Snapshot diagrams

### primitive values

### object values



![image-20240221143526266](C:\Users\think\AppData\Roaming\Typora\typora-user-images\image-20240221143526266.png)

object 用 圈表示， primitive 用字母表示， 值用 箭头表示



## mutating values vs. reassigning variables

重新赋值 vs 更改元素

![image-20240221143912039](C:\Users\think\AppData\Roaming\Typora\typora-user-images\image-20240221143912039.png)

## == vs. equals()

== 对于 object 来说，对比的是其引用地址

.equals 对比的是其值。



# Java Collections

### list

| Java                      | description                  | Python             |
| :------------------------ | :--------------------------- | :----------------- |
| `int count = lst.size();` | count the number of elements | `count = len(lst)` |
| `lst.add(e);`             | append an element to the end | `lst.append(e)`    |
| `if (lst.isEmpty()) ...`  | test if the list is empty    | `if not lst: ...`  |

### Map

| Java                   | description                    | Python           |
| :--------------------- | :----------------------------- | :--------------- |
| `map.put(key, val)`    | add the mapping *key → val*    | `map[key] = val` |
| `map.get(key)`         | get the value for a key        | `map[key]`       |
| `map.containsKey(key)` | test whether the map has a key | `key in map`     |
| `map.remove(key)`      | delete a mapping               | `del map[key]`   |

### Set

| Java                 | description                         | Python                                |
| :------------------- | :---------------------------------- | :------------------------------------ |
| `s1.contains(e)`     | test if the set contains an element | `e in s1`                             |
| `s1.containsAll(s2)` | test whether *s1 ⊇ s2*              | `s1.issuperset(s2)` `s1 >= s2`        |
| `s1.removeAll(s2)`   | remove *s2* from *s1*               | `s1.difference_update(s2)` `s1 -= s2` |

### literals

python 可以直接通过 【】 创建列表

java的 `String[] arr = { "a", "b", "c" };` 创建的是array， 

而如果想要创建 list、set、map的话，需要使用

```java
List.of("a", "b", "c");
Set.of("a", "b", "c");
Map.of("apple", 5, "banana", 7);
```

### 泛型创建 generics

```java
List<String> cities;
Set<Integer> numbers;
Map<Sring, Turtle> turtles;
```



## ArrayLists and LinkedLists: creating Lists

`List`, `Set`, `Map` 是 interface， 不包含具体实现，而 `ArrayList` 和 `LinkedList` 则是具体实现。 



### HashSets and HashMaps: creating Sets and Maps



## Java API documentation

[Overview (Java SE 12 & JDK 12 ) (oracle.com)](https://docs.oracle.com/en/java/javase/12/docs/api/index.html)