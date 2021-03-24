# git 常用命令

注：<>内的表示注释内容，非命令

git init：初始化本地仓库

git clone ：检出远程分支到本地

git add "文件名" ：添加到本地仓库

git commit -am "说明" ：提交分支。加的-a参数可以将所有已跟踪文件中的执行修改或删除操作的文件都提交到本地仓库，即使它们没有经过git add添加到暂存区

git commit -o 指定文件名 -m '备注'  ：#提交指定文件

 

git log ：查看历史记录 ，可以查看到提交的版本号

git log --graph： 查看历史记录分支明细

 

git branch：查看分支

git branch -r：查看远程分支

git branch <name>：创建分支

git checkout <name>：切换分支

git checkout -b <branch name>：创建+切换分支，没有-b则只创建分支

git merge --no-ff  <branch name>：合并某分支到当前分支。不加--no-ff表示快速合并，加了该参数会有合并日志记录

 

git branch -d <branch name>：删除分支

git branch -D <branch name>：强行删除分支

git push origin --delete < branch  name>：删除远程分支

git reset --hard HEAD^：来回退到上一次commit的状态

git reset --hard  commitid：此命令可以用来回退到任意版本

 

git remote -v：查看远程分支情况

git push -u origin：推送分支到远程；-u表示指定一个默认主机，后面push可以直接git push

 

git update-index --assume-unchanged <文件名>：git忽略跟踪某文件

git config --list ：查看所有git配置

git config user.name：查看自己的用户名和

git config user.email：查看自己的邮箱地址

git config --global user.name "xxx"：修改自己的用户名

git config --global user.email "xxx"：修改自己的邮箱地址

 

git stash 取消了仓库里的文件修改



git clean -d -fx：表示删除 一些 没有 git add 的 文件；打开SourceTree通过命令行，进入本地版本仓库目录下，直接执行

git clean 参数 ：

    -n 显示将要删除的文件和目录；
    -x -----删除忽略文件已经对git来说不识别的文件
    -d -----删除未被添加到git的路径中的文件
    -f -----强制运行
where git：查找本地git程序安装路径

 

Git diff branch1 branch2 --stat                 //显示出所有有差异的文件列表

Git diff branch1 branch2 文件名(带路径)   //显示指定文件的详细差异

Git diff branch1 branch2                          //显示出所有有差异的文件的详细差异
