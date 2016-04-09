1.概念
```
工作区:电脑里的目录
版本库:工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。
暂存区:add后需要提交的文件临时存储区
本地分支:commit后提交到git为我们自动创建的第一个分支master，HEAD指向master
HEAD:当前活跃分支的游标。形象的记忆就是：你现在在哪儿，HEAD 就指向哪儿，所以 Git 才知道你在那儿。
```

2. 新建.git文件
```
git init
```

3.暂存区(stage或者index)：
```
git add filename //提交文件到缓存区
git add .   //提交所有改动到缓存区
.gitignore  //忽略:里面写正则表达式忽略文件名

node_modules
.idea
.svn
```

4.提交本地分支

git commit -m "代码提交信息"  //提交到head仓库

5.查看日志
```
git log
git log --pretty=oneline    //忽略更多提示信息
```


6.推送远程版本
```
git remote rm origin                       //删除推送地址重新设置
git remote add origin https://594237406:jdkn45263@github.com/594237406/senior.git
git push origin master                   //推送到远程地址
```

7.删除文件
```
git rm filename        //提交后无法找回
rm filename            //提交后无法找回
```
8.查询关键字
git grep xxx







