1. 新建.git文件

```
git init
```


2. 暂存区：

```
git add filename //提交文件到缓存区
git add .   //提交所有改动到缓存区
.gitignore  //忽略:里面写正则表达式忽略文件名

node_modules
.idea
.svn
```


3.缓存区index

git commit -m "代码提交信息"  //提交到head仓库

4.查看日志
git log
git log suppress summary


4.git remote add origin 远程推送地址        //只对init目录执行，设置远程提交地址

5.git push origin master                   //推送到远程地址

6.git status                               //看状态

7.不用输入用户名密码，方法：

git remote rm origin                       //删除推送地址重新设置

git remote add origin https://594237406:jdkn45263@github.com/594237406/senior.git


8.add与commit合并:git commit -a -m ""

9.更新代码 git pull

10.对比代码 git diff

11.删除远程分支
git branch -r -d origin/branch-name

不成功，发现只是删除的本地对该远程分支的track，正确的方法应该是这样：

git push origin :branch-name

冒号前面的空格不能少，原理是把一个空分支push到server上，相当于删除该分支。

12.推送到远程分支
git push origin test

13.查看远程分支
git branch -a

14.下载远程分支
git checkout -b online origin/release/online



