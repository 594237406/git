1.git fetch：相当于是从远程获取最新版本到本地，不会自动merge
```
git fetch origin master
git log -p master..origin/master
git merge origin/master

git fetch origin master:tmp
git diff tmp
git merge tmp
```

2.git pull：相当于是从远程获取最新版本并merge到本地
上述命令其实相当于git fetch 和 git merge
在实际使用中，git fetch更安全一些
因为在merge前，我们可以查看更新情况，然后再决定是否合并