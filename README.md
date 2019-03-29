# some-Tips

通过VI编辑器修改host：
输入sudo vi /etc/hosts 提示输入密码并回车


切换node版本：
直接 输入sudo n，输入密码， 会出现你所安装的所有版本，上下键选择，按回车，搞定
sudo n
node -v


代码冲突解决流程：
1、git checkout master
2、git pull origin master
3、git checkout 当前分支
4、git rebase origin/master
5、右点击项目->Git ->resolve
6、确认后点apply
7、git add .
8、git rebase —continue
9、git add .
10、git commit —amend


查看是否有冲突
git stash pop stash@{0}


把一个分支的代码移动另一个分支上：
1、首先取到该分支的ID，使用git log
2、checkout到新的分支上，然后 git cherry-pick ID


删除已经提交的一个文件：
1、git log 拿到不是本次提交的ID，
2、git reset ID
3、git checkout 不要提交的文件


git自动补全功能
	1、下载git代码库：
		git clone https://github.com/git/git.git
	2、创建~/.git-completion.bash：
		cp git/contrib/completion/git-completion.bash ~/.git-completion.bash
	3、修改~/.bash_profile（没有则创建）
		vim ~/.bashrc
		添加如下内容：
		source ~/.git-completion.bash
	4、重启终端 

