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
git checkout filename      //如果没有添加到暂存区撤销工作区修改,还原到上一个版本.如果添加到暂存区,还原到暂存区.如果文件被删除,重新下载
git reset --soft id        //回退到commit,工作区和暂存区不做变化
git reset --mixed          //默认,回退到index,工作区不做变化
git reset --keep           //回退到add,保留已经提交到index的修改和没有提交到index上的修改
git reset --merge          //pull后本地产生冲突,回退到commit,保持本地没有提交到index的修改
git reset --hard HEAD^     //HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100
git reset --hard 3628164   //回退到某个版本号,本地修改丢失
git reflog //查看历史命令
```

7.推送远程版本
```
git remote rm origin                       //删除推送地址重新设置
git remote add origin https://594237406:jdkn45263@github.com/594237406/senior.git
git push origin master                   //推送到远程地址
```

8.删除文件
```
git rm filename        //提交后无法找回
rm filename            //提交后无法找回
```







