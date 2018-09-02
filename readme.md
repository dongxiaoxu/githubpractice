pratice use git and github

git init ：初始化本地仓库，使用该命令后才能进行git的操作（当然，使用git clone 从远程仓库后已进行init）

git add : 提交文件到暂存区（先暂存，再提交）

git commit -m '备注': 提交到本地仓库（git commit -a -m '备注' 可一次执行git add 和git commit ）

git branch : 查看分支

git branch branchname : 新建分支

git branch -d branchname : 删除分支（当分支有未合并的文件时删除会失败，如果要强制删除，使用 -D 选项）

git checkout branchname : 切换分支

git tag : 查看标签

git tag tagname : 新建标签

git tag -d tagname : 删除标签

git checkout tagname : 切换标签




config logdetail command shutcut:git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%
d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"