Git is a distributed version control system.
Git is free software,distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes.
1.自报家门
2.初始化仓库，添加文件,查看状态
3.穿越远古，返回未来
4.理解暂存区stage


Unix的哲学是“没有消息就是好消息”，说明添加成功
千万不要使用Windows自带的记事本编辑任何文本文件。
版本控制系统设计得优秀：因为Git跟踪并管理的是修改
git status：随时掌握仓库(工作区)的状态；
git diff：查看修改内容(difference)；
git log：查看提交历史(从最近到最远)，只能回到从前；
git reflog；查看命令历史，能回到未来；
git log --pretty=oneline：(commit_id版本号)提交的说明
git reset --hard HEAD^：版本回退(head指当前版本，^前一个，^^前两个，~100前一百个)；
git reset --hard 版本号前n位：(后悔穿越了，窗口还没关)指定回到未来的某个版本；

cat 文件名：显示文件内容；

