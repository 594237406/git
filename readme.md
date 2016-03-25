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

6.版本回退
```
git reset --soft id        //回退到commit,工作区和暂存区不做变化
git reset --mixed          //默认,回退到index,工作区不做变化
git reset --keep           //默认,回退到add,保持本地修改
git reset --merge          //pull后本地产生冲突,回退到commit,保持本地没有提交到index的修改
git reset --hard HEAD^     //HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100
git reset --hard 3628164   //回退到某个版本号,本地修改丢失
git reflog //查看历史命令
```

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



