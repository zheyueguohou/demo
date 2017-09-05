# demo

git使用方法：https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013752340242354807e192f02a44359908df8a5643103a000

1、首先在github创建仓库 git@github.com:zheyueguohou/demo.git

如果在github的remote上已经有了文件，会出现错误。此时应当先pull一下，即：git pull origin master

初始化命令：
git init
git add . 
git commit -m 'first commit'
git push origin master


git常用命令

【基本命令】

mkdir 创建文件cd file 进入文件
git init 把这个目录变成git可以管理的仓库，生成.git文件
git add readme.txt 把文件添加到仓库
git commit -m "whrote a readme file" 提交到仓库
git status  查看仓库当前的状态，告诉readme.txt修改过了，但是还没有准备提交
git diff readme.txt 显示变更类似linux diff命令
git log 显示提交的日志
git log --pretty=oneline 显示提交日志精简版
git reset --hard commit_id 回退到提交的版本
git reflog 查看commit_id供回退用
git reset --hard HEAD^ 回退到上一个操作id
git checkout -- readme.txt 撤销修改一定要加--
git reset HEAD file 撤销暂存区的修改
git rm test.txt 从版本库中删除文件
git branch <name> 创建分支
git checkout <name>  切换分支
git checkout -b <name> 创建+切换分支
git branch 查看分支
git merge dev 合并dev分支到当前主分支
git branch -d <name> 删除分支
git stash 把当前工作现场储藏起来
git stash list 查看存储的工作现场
git stash apply/drop 回复/删除
git stash pop 恢复并删除
git remote 查看远程库信息
git remote -v 查看远程库详细信息
git push origin master 推送分支到远程库
【多人写作模式】

git push origin branch-name 推送自己的修改
git pull 合并
git branch --set -upstream branch-name origin/branch-name 建立本地分支和远程分支连接
【打标签】

git branch
git checkout master
git tag v1.0 给该分支打标签
git tag 查看所有标签
git log --pretty=oneline --abbrev-commit 查看历史提交id
git tag v0.9 6224937 给该id打标签
git tag 查看标签
git show v0.9 查看标签
git tag -a v0.1 -m "version 0.1 relased" 3628164 -a标签名 -m说明文
git tag -s v0.1 -m "version 0.1 relased" 3628164 -s用私钥签名 -m说明文字
git tag -d v0.1 删除标签
git push origin v1.0 推送某个标签到远程
git push origin --tags 推送所有标签

错误信息：
1、Everything up-to-date
原因：
1）没有git add .
2）没有git commit -m "提交信息"

2、error: src refspec master does not match any.
error: failed to push some refs to 'https://github.com/zheyueguohou/demo.git'
空目录不能推送，先add、commit、后pull

