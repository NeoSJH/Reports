
**配置用户和邮件**
git config --global user.name "git用户名"
git config --global user.email "git的邮箱"
**初始化**
git init：初始化git,添加本地仓库
git status：查看文件有没有被追踪， 查看分支，即未提交到远程仓库的文件，工作区
git add + 添加的文件名：添加指定文件到本地仓库
git add  : 使用git add + 点，可以将所有文件添加到本地仓库
git commit ：添加到远程仓库
git commit -m + 注释 ：提交，并添加本次提交的注释
git remote add  [shortname] [url] : 添加远程仓库 ,用一个shortname作为url地址的远程仓库的代称
git log：查看提交
git push -u [远程仓库名] master ：将本地分支的更新，推送到远程主机
例：git remote add 仓库名 https://github.com/git用户名/本地仓库文件名git后缀

例如
git init   初始本地仓库
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:NeoSJH/Reports.git
git push -u origin master

ls -a :查看文件夹目录下的文件
git config --list : 查看配置情况

**撤销**
git commit --amend: 插销上一次的提交，重新提交
gti checkout -- + 文件名：可以把本地文件修改为远程仓库上的那个版本的文件
git checkout -- . :将全部文件从远程仓库上恢复


**git push -u origin master发生fatal: Could not read from remote repository：**
因为SSH的原因，需要删除当前key，然后重新生成key
在git命令端输入指令：ssh-keygen -t rsa -C "邮箱地址"，它会在本地C:\Users\你的用户名.ssh生成文件夹，里面有id_rsa和id_rsa.pub两个文件 ，然后复制id_rsa.pub文件里面的内容，到https://github.com/settings/keys新建一个即可 

