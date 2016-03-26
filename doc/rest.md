1.版本回退
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