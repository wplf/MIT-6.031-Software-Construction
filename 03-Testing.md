# 03-Testing

## Target

- 理解测试的价值
- 能判断测试 test suite 的正确性、完备性和复杂度
- 能根据输入的空间设计测试套装
- 能判断测试范围，理解什么时候用 black box、glass box、unit test、integration test 和 自动回归test。

​            ![image-20240221192421732](C:\Users\think\AppData\Roaming\Typora\typora-user-images\image-20240221192421732.png)

## 使用 JUnit 自动测试

`java` 中的 `JUnit` 可以方便的测试代码正确性，其内部通常包含 `assertEquals` 函数，例如

```java
public class MaxTest {
    @Test
    public void testALessThanB() {
        assertEquals(2, Math.max(1, 2));
    }
	@Test
    public void testDrawFromSet() {
      Set<Integer> set = Set.of(293, 384, 10, 5, -3, 99);
      int result = pickRandomly(set);
    assertTrue(set.contains(result), "expected result to be from " + set + " but actually was " + result);
    }
}
```



## 记录测试方案

```java
public class MaxTest {
  /*
   * Testing strategy
   *
   * partition:
   *    a < b
   *    a > b
   *    a = b
   */
}
```



## 黑盒测试和白盒测试 

black box and glass box testing

黑盒测试是根据 函数的定义，specification 设置测试样例，并不清楚函数实现方式

白盒测试是根据函数实现方式，设置测试样例。



### Coverage

**statement coverage**： 语句覆盖率，代码中的每个语句是否会被执行

**Branch coverage**： 分支覆盖率

**Path coverage**： 分支中的每个组合是否都覆盖， 指数级的复杂度

http://www.eclemma.org/ 是一个非常好的测试工具。



## Unit and integration testing

单元测试与整合测试



## Automated regression testing

自动测试：如题

回归测试：每次对代码做改动都使用所有的 test case 进行测试

## Iterative test-first programming

编写函数定义

迭代修改测试样例和函数规范



## 小结：

1. 写程序之前先写测试样例
2. 分割测试样例和边界条件， 针对性进行系统测试
3. 白盒测试 + 测试 语句覆盖率
4.  对每个module 进行 unit test
5. 自动回归测试， 每次更改代码都要进行 test
6. 迭代版本开发
