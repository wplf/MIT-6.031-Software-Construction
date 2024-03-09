# 14-Debugging

# Summary

- reproduce the bug as a test case, and put it in your regression suite
- find the bug using the scientific method:
  - generate hypotheses using slicing, binary search, and delta debugging
    - slice 的意思是将 变量的组成因素变小， 例如 `x=a+b+c`, 检查的时候去看 `x=a+b`
    - delta debugging 的意思是 不断缩小 bug 出现的范围，去除 无效函数。
  - use minimially-invasive probes, like print statements, assertions, or a debugger, to observe program behavior and test the prediction of your hypotheses
- fix the bug thoughtfully