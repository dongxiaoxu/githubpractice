pratice use git and github

git log : 提交日志

git status : 当前仓库状态

git init ：初始化本地仓库，使用该命令后才能进行git的操作（当然，使用git clone 从远程仓库后已进行init）

git add : 提交文件到暂存区（先暂存，再提交）

git commit -m '备注': 提交到本地仓库（git commit -a -m '备注' 可一次执行git add 和git commit ）

git branch : 查看分支

git branch branchname : 新建分支(新建分支的命令是基于当前所在分支的基础上进行)

git branch -d branchname : 删除分支（当分支有未合并的文件时删除会失败，如果要强制删除，使用 -D 选项）

git checkout branchname : 切换分支

git merge branchname : 合并分支（注意在合并分支前必须切换到master分支）

git tag : 查看标签

git tag tagname : 新建标签

git tag -d tagname : 删除标签

git checkout tagname : 切换标签

git config --global alias.aliasname 'gitcommand' : 配置git操作的别名

配置详细日志别名:git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%
d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"

git clone 'remoteresponsity' : 从远程仓库拉取（通过http或ssh协议）