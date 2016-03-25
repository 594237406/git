1.比较的是工作目录(Working tree)和暂存区域快照(index)之间的差异
    git diff

2.显示的是下一次commit时会提交到HEAD的内容(不带-a情况下)
    git diff --cached
    git diff --staged

3.显示工作版本(Working tree)和HEAD的差别
    git diff HEAD

4.直接将两个分支上最新的提交做diff
    git diff branch1 branch2

5.输出自topic和master分别开发以来，master分支上的changed。
    git diff topic...master

6.查看简单的diff结果，可以加上--stat参数
    git diff --stat

7.查看当前目录和另外一个分支的差别
    git diff test

8.比较上次提交commit和上上次提交
    git diff HEAD^ HEAD

9.比较两个历史版本之间的差异
    git diff id1 id2