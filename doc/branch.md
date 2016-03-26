
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
//查看所有分支
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
```
git push origin master  //把本地分支推送到远程分支上
```

6.下载远程分支
```
git checkout -b dev origin/dev
```

7.建立本地分支与远程分支链接
```
git branch --set-upstream branch-name origin/branchname
```

8.查看分支合并图
```
git log --graph
```

9.禁用Fast forward
```
//如果A,B分支都做修改,则会产生a,b两个版本,合并后产生c版本
git merge --no-ff b  //把b合并到a版本,不会产生c版本
```