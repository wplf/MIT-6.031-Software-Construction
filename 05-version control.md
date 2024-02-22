## 05 - version control

version control system 的特点

1. 可靠
2. 多文件
3. 有意义的版本
4. 可以复原
5. 能够比较不同版本
6. 查看历史
7. 可以记录 image pdf等其他文件



version 的功能

1. merge 
2. track responsibilities
3. work in parallel
4. work in progress



```bash
git config --global alias.lol "log --graph --oneline --decorate --color --all"

git lol
git show               #可以查看修改的内容
git show [hash]        #查看修改的内容
git show [hash]:       #查看这次提交有的文件
git show [hash]:[filename] #查看提交文件的内容
```

