 - **git config --global user.name "zmz"**
- **git config --global user.email "zmzsstreet@163.com"**
  ### 配置用户信息
git init  初始化
git add hello.txt
添加到暂存区
git commit
提交到仓库
git log
查询提交记录
git log --oneline
一个记录显示一行
git log --graph
查看分支合并图
git reflog
hash值显示比较短

git reset --hard 记录哈希值
恢复到指定记录
git reset --hard HEAD^
恢复到上一记录
git reset --hard~3
后退三步

git reset HEAD 1.txt
恢复到HEAD指针当前所指的值 
git chechout -- 1.txt
丢弃工作区的修改     即恢复到上次commit状态中间没有add
git reset HEAD <file>
把暂存区的修改撤销掉（unstage），重新放回工作区
git rm 1.txt
将1.txt清除 

git diff 文件名
查看当前文件和暂存区差异
git diff 本地库历史版本  文件名
工作区与本地库比较
不带文件名 比较所有文件


git branch -v
查看分支状态
git branch hot_fix
创建一个名为hot_fix的新分支
git checkout hot_fix
切换到hot_fix分支
git merge hot_fix
将hot_fix分支的动作合并到当前分支
git checkout命令加上-b参数表示创建并切换，相当于以下两条命令
git branch dev
git checkout dev
====
git branch -d dev
删除dev分支

git remote -v
查看远程仓库信息
git remote add origin git@github.com:zhaomanzhou/work.git
添加远程仓库
git remote rm origin
删除远程地址
git push origin master
推从到远程仓库


git pull origin master
从origin master分支源获取最新提交并合并

git pull相当于git fetch + git merge

git fetch origin master:tmp
从origin master分支源获取最新提交到本地tmp分支

git rebase
本地修改提交，远程仓库比本地仓库提前，从远程仓库pull一下
然后运行git rebase 会把本地提交置于 pull后提交之后

tail -n 3 文件名
显示文件最后三行
