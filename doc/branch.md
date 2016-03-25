
1.创建并切换分支
```
//创建分支
git branch branchname
//切换分支
git checkout branchname
//创建切换分支
git checkout -b dev
//相当于
//git branch dev
//git checkout dev
```

2.查看分支
```
//查看本地分支
git branch
//查看远程分支
git branch -a
```

3.合并分支
```
//修改内容,提交
//切回master分支
git merge dev
```

4.删除分支
```
//删除本地分支
git branch -d branchname
//删除远程分支
git branch -r -d origin/branchname
git push origin :branch-name
```


5.推送到远程分支
git push origin test

6.下载远程分支
git checkout -b dev origin/dev

7.建立本地分支与远程分支链接
git branch --set-upstream branch-name origin/branch-name