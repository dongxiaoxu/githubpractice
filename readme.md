pratice use git and github

git log : 提交日志

git reflog : 操作日志

git status : 当前仓库状态

git init ：初始化本地仓库，使用该命令后才能进行git的操作（当然，使用git clone 从远程仓库后已进行init）

git add : 提交文件到暂存区（先暂存，再提交）

git commit -m '备注': 提交到本地仓库（git commit -a -m '备注' 可一次执行git add 和git commit ）

git branch : 查看分支

git branch branchname : 新建分支(新建分支的命令是基于当前所在分支的基础上进行)

git branch -d branchname : 删除分支（当分支有未合并的文件时删除会失败，如果要强制删除，使用 -D 选项）

git checkout branchname : 切换分支

git merge branchname : 合并分支

git tag : 查看标签

git tag tagname : 新建标签

git tag -d tagname : 删除标签

git checkout tagname : 切换标签

git config --global alias.aliasname 'gitcommand' : 配置git操作的别名

配置详细日志别名:git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%
d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"

git clone 'remoteresponsity' : 从远程仓库拉取（通过http或ssh协议）

命令git tag <tagname>用于新建一个标签，默认为HEAD，也可以指定一个commit id；

命令git tag -a <tagname> -m "blablabla..."可以指定标签信息；

命令git tag可以查看所有标签。

命令git push origin <tagname>可以推送一个本地标签；

命令git push origin --tags可以推送全部未推送过的本地标签；

命令git tag -d <tagname>可以删除一个本地标签；

命令git push origin :refs/tags/<tagname>可以删除一个远程标签。

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

删除远程分支： git push -d origin <branchname>

查看远程库信息，使用git remote -v；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；

在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；

从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。

/*************************************

多人协作的工作模式通常是这样：

首先，可以试图用git push origin <branch-name>推送自己的修改；

如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；

如果合并有冲突，则解决冲突，并在本地提交；

没有冲突或者解决掉冲突后，再用git push origin <branch-name>推送就能成功！

如果git pull提示no tracking information，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream-to <branch-name> origin/<branch-name>

*************************************/