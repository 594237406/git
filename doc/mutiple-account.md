1. 创建多少个账号，命名时候把id_rsa改下名字

	```
	ssh-keygen -t rsa -C "your-email-address" 
	#存储key的时候，不要覆盖现有的id_rsa，在生成两个Key时，不要随便输入enter键就就不会覆盖掉老的两个key ,
	使用一个新的名字，比如id_rsa_work 
	```

2. 把该key加到ssh agent上。由于不是使用默认的.ssh/id_rsa，所以你需要显示告诉ssh agent你的新key的位置

	```
	ssh-add ~/.ssh/id_rsa_work
	#可以通过ssh-add -l来确认结果 
	```

3. 配置.ssh/config 

	```
	Host gitlib
	  HostName gitlab.alipay-inc.com
	  PreferredAuthentications publickey
	  IdentityFile ~/.ssh/id_rsa
	
	Host github
	  HostName github.com
	  PreferredAuthentications publickey
	  IdentityFile ~/.ssh/id_rsa.github
	```
	
4. 检查
	```
	ssh -T git@gitlib/github(Host)
	```
		