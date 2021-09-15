
# 如何将本地仓库上传到github

1. github上新建仓库，拷贝仓库ssh地址
2. 本地电脑生成ssh key `ssh-keygen -t rsa -b 4096 -C "youremail"`，然后在github账户中添加公钥
3. .ssh/config 中配置秘钥
	```
	Host github.com
	Preferredauthentications publickey
	IdentityFile ~/.ssh/生成的秘钥
	```
3. 验证设置是否生效：终端输入 `ssh -T git@github.com`，验证失败时可通过`ssh -vT git@github.com`查看报错
4. 项目根目录下执行 `git remote add origin git@github.com:xxx/xxx.git`
5. 执行 `git push -u origin master`
6. 如果使用SourceTree/Fork等软件，需要配置项目的用户信息和github账户对应
