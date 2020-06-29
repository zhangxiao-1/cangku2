Git是一个开源的分布式版本控制系统，用以有效、高速的处理从很小到非常大的项目版本管理。

- 全称：GNU Interactive Tools
- 适用人群：本教程绝对面向初学者，没有接触过版本控制概念的读者也可以轻松入门

> ### 进入项目，右击选择Git Bash Here

1. git配置：git config --global user.name "Gaojiao"
           			  git config --global user.email "2011747643@qq.com"

2. 代码每次修改，都需要修改：
           当前目录全部放到暂存区：git add 文件名/.（.全部文件）
           提交到本地仓库分支上：git commit -m"提交描述"

3. 创建仓库：git init

4. 检查git仓库的状态：git status

5. 检查所进入文件夹的文件目录：ls

6. 版本回退：查看版本的日志（提交的历史）：git log
       			（命令历史）：git reflog
       			回退到某个版本：git reset --hard commit_id（提交的id）

7. 组件恢复到最初版本：进入需要恢复的文件夹中，git checkout -- 组件名

8. dev分支：仓库的备份，想保存代码，但不想提交到仓库时，可以提交到仓库分支上

   ​				创建并切换：git checkout -b 分支名
   ​       		 查看当前分支：git branch
   ​        		切换到已有分支：git checkout 分支名
   ​        		删除分支：删除时切换到主分支git checkout master，进行使用git branch -d 分支名
   ​        		合并某分支到当前分支master：git merge 分支名
   ​        		看到分支合并图（无法自动合并时）：git log --graph

> ### 远程仓库：

1. 创建仓库（不要勾选自述文件README.md)
2.  在本地仓库添加远程仓库地址：git remote add origin 地址（在git仓库里复制）
3. 修改本地仓库提交到地址：git 
4. 推送到远程仓库（拉取）：git pull origin master
5. 推送到远程仓库（提交）：git push -u origin master

> ### 创建SSH Key：

$ ssh-keygen -t rsa -C "youremail@example.com"

> ### 共同开发项目（克隆）

1. 组长给你一个git仓库地址  （里面有你要开发的项目）
1. 克隆到本地 git clone 地址
1. 组长添加你为协作了
1. 本地仓库添加远程仓库地址
2. 修改代码
1. 提交之前一定要pull 拉去最新的代码
1. 提交到本地仓库 在提交到远程仓库 
1. 可能会冲突 共同修改了同一个文件

> ### 工作区和暂存区

Git 和其他版本控制系统如 SVN 的一个不同之处就是有暂存区的概念。

- 工作区：没有提交到暂存区的项目
- 暂存区：通过git add添加的文件进入暂存
- 仓库分支：通过git commit -m进入分支