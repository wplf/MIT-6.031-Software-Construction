# 08-Mutability & Immutability

可变的好处：

- 在 append 时，不会多次开辟内存

- 对iterator来说， 元素长度不统一会产生bug。
- 可变会让代码很难修改

不可变的好处

- 不会出现 alias 的bug
- 变量的含义不会变， easy to understand
- 代码很好改，其他依赖于该变量的函数按以前的格式调整即可。