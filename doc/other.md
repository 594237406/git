1.Git还提供了一个stash功能，可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作.stash后,工作区和缓存区保持与版本库一致
```
git stash       //缓存当前文件
git stash list  //查看缓存区文件
git stash apply //不清空缓存,恢复文件
git stash pop   //清空缓存,恢复文件
```