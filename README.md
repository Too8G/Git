# GIT 笔记
#### 设置用户名和邮箱
GIT是分布式的，每个节点(机器)都要自报家门：用户名+邮箱。  
设置全局用户名、邮箱（USERHOME/.gitconfig）  
`git config --global user.name "Your Name"`  
`git config --global user.email "email@example.com"`  
查看全局用户名、邮箱  
`git config --global user.name`  
`git config --global user.email `  
设置指定仓库的用户名、邮箱（仓库/.git/config）  
`git config user.name "username"`  
`git config user.email "email"`  
`git config user.name`  
`git config user.email `  
#### 简单操作  
在一个目录下执行命令，则这个目录就变为git的仓库了，会生成.git  
`git init`  
文件添加到仓库  
`git add filename`  
全部添加  
`git add .`   
执行后没有返回信息，Unix的哲学是“没有消息就是好消息”  
文件提交到仓库  
`git commit [filename] -m "wrote a readme file"`  
查看当前仓库中文件状态  
`git status`  
比较工作区和暂存区差异  
`git diff [filename]`  
比较暂存区和分支差异  
`git diff --cached [filename] `  
查看修改日志  
`git log [--pretty=oneline] [filename]`  
回退到前N个版本（N个^）（HEAD是当前版本的指针）  
`git reset --hard HEAD^`  
注意在windows cmd中，^是转义字符，需要写成 "^" 或者 ^^  
回退到指定版本号（一般用版本号前6位，模糊匹配的）  
`git reset --hard 版本号前N位`  
查看历史命令记录  
`git reflog`  
撤回工作区（回退成暂存区或分支最新版本）  
`git checkout -- filename`  
回退暂存区（回退到分支最新版本）  
`git reset HEAD filename`  
git reset即可以回退版本，也可以回退工作区。  
GIT是分布式存储，在你没有推送到远端之前，在本地的版本（工作区、暂存区、分支）都可以改。  
删除文件  
`git rm filename`  
`git commit filename -m "desc"`  

#### 一些概念  
工作区（Working Directory）：当初执行git init的那个目录，除了.git的所有内容。  
版本库（Repository）：.git里面的内容。  
git add 命令，将文件提交暂存区（stage or index）。  
git commit 命令，将暂存区内文件提交到分支（branch）。  
#### GITHUB
GITHUB远程GIT仓库，https://github.com/  
本地git和github是ssh传输，先设置ssh。  
1、用户主目录/.ssh/id_rsa、id_rsa.pub，如果没有则生成  
`ssh-keygen -t rsa -C "youremail@example.com"`  
可以不用设置密码  
2、在GITHUB后台设置公钥(id_rsa.pub)。这样就能确认是你提交的了。
关于同步  
1、在github上创建一个仓库（New Repository），然后 Clone or download会显示：  
  git@github.com:Too8G/Git.git  
2、关联远程版本库（origin是远程版本库的名字，可以改。只针对本地当前版本库有效）  
`git remote add origin git@github.com:Too8G/Git.git`  
3、将本地版本库推送到远程版本库指定分支（如果没有关联，会提示无法识别 origin）
`git push -u origin master`  
推送到远程版本库origin的master分支。第一次用-u是把本地master分支和远程master分支关联起来。以后就不用了。  
我本地报错了，因为版本库上有相同的文件，需要先pull，再push。  
4、从远程版本库拉下来  
`git pull origin master`  
有冲突，先从远程把最新的pull下来，修改后，在push上去。  



