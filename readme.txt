Git is a distributed version control system.
Git is free software,distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
My stupid boss still prefers SVN.
Creating a new branch is quick and simple.
1.自报家门
2.初始化仓库，添加文件,查看状态
3.穿越远古，返回未来
4.理解：工作区-->(暂存区stage)-->master;
5.管理修改
6.删除文件(rm 类似 add，比较绕)：工作区删除了rm，即修改，要更新到暂存区git rm，再更新到版本库git commit。
7.远程库：了解+关联+克隆
8.使用分支：创建+切换，...，提交，切换，合并，删除
9.解决冲突：已放在版本库的feather和master内容冲突，发生merge failed后，冲突的文件中会显示两者；修改后，重新add+commit；删除feather指针；可以看分支合并图；
10.分支管理智慧：合并分支时，Git会默认Fast forward模式，删除分支后，会丢掉分支信息。强制禁用Fast forward模式，Git在merge时生成新的commit，分支历史上会保留分支信息。
11.

Unix的哲学是“没有消息就是好消息”，说明添加成功
千万不要使用Windows自带的记事本编辑任何文本文件。
版本控制系统设计得优秀：因为Git跟踪并管理的是修改
撤销提交了的错的修改到版本库：(本地版本还没有推送到远程库)版本回退；
其实一台电脑上也是可以克隆多个版本库的，只要不在同一个目录下。
有了远程仓库，妈妈再也不用担心我的硬盘了。”——Git点读机
确认指纹信息是否真的来自GitHub的服务器，输入yes。
？？HEAD指向的就是当前分支，master指向最新提交，
创建、合并和删除分支非常快，所以用分支完成某个任务，合并后再删掉分支，(直接在master分支上工作效果一样)过程更安全;
？？怎么比较两个指针指向的内容的差别


git status：随时掌握仓库(工作区)的状态；
git diff：查看修改内容(difference)，暂存区[退一步就是版本库]:工作区，绿色字体是新的；
  git diff HEAD -- readme.txt：查看版本库和工作区的区别；
git log：查看提交历史(从最近到最远)，只能回到从前；
  git log --pretty=oneline：(commit_id版本号)各次提交的记录；
git reflog；查看历史，能回到未来；

git checkout -- 文件名：取回暂存区[退一步就是版本库]替代工作区。

git reset --hard HEAD^：工作区版本回退(head指当前版本，^前一个，^^前两个，~100前一百个)，清空暂存区；
  git reset --hard 版本号前n位：指定回到未来的某个版本，清空暂存区；
git add/rm 文件名：工作区记录存入暂存区；
git reset HEAD 文件名：删除暂存区的记录，不影响工作区；

git init	初始化空版本库；
git commit -m "说明"	提交即更新版本库；
git push origin master：本地提交上远程库，就可以通过命令：
git clone 地址：	克隆远程库；
git branch：	列出所有分支，当前分支前标有*；
git branch 分支名：	创建分支(在当前分支处)；
git checkout 分支名：	切换分支;
git checkout -b 分支名：	创建分支，切换到该分支
git merge 分支名dev:	master下(未详细了解，先保证暂存区为空)，合并某dev分支到当前分支master；即master=dev；
git branch -d 分支名：	删除某分支；
git log --graph --pretty=oneline --abbrev-commit：	查看简要的分支合并图；


pwd (print working directory)现实工作目录
ls	显示文件
cat 文件名：显示文件内容；
cd	cd..	cd / 文件游览
