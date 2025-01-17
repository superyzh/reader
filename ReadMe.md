
# 先更新再提交（先pull，再push）

# create a new repository on the command line
## git init
## git add README.md
## git commit -m "first commit"
## git remote add origin https://github.com/superyzh/reader.git
## git push -u origin master

#  push an existing repository from the command line
## git remote add origin https://github.com/superyzh/reader.git
## git push -u origin master

#从远程分支拉取代码到本地  
## git pull https://github.com/superyzh/reader  master  


# git commit、git push、git pull、 git fetch、git merge 的含义与区别

## git commit：是将本地修改过的文件提交到本地库中；
## git push：是将本地库中的最新信息发送给远程库；
## git pull：是从远程获取最新版本到本地，并自动merge；
## git fetch：是从远程获取最新版本到本地，不会自动merge；
## git merge：是用于从指定的commit(s)合并到当前分支，用来合并两个分支；



1.  安装完成后，在开始菜单里找到“Git”->“Git Bash”

2.  git config --global user.name "Your Name"
    git config --global user.email "email@example.com"

3.  cd F: (打开F盘)
    mkdir <name> (创建子目录)
    pwd (显示当前目录)

4.  git init (把这个目录变成Git可以管理的仓库)

5.  git add <file>

6.  git commit -m "说明"

7.  git status (仓库当前的状态)

8.  git diff (查看不同)

9.  git log [--pretty=oneline  {缩略版,可选}] (查看历史记录)

10. git reset --hard HEAD^ (回退到上一个版本,HEAD后可以是 commit_id)

11. git reflog (用来记录你的每一次命令,找到commit_id回到未来某个版本)

12. git diff HEAD -- <file> (查看工作区和版本库里面最新版本的区别)

13. git checkout -- <file> (用版本库里的版本替换工作区的版本，无论工作区是修改还是删除)

14. git reset HEAD <file> (把暂存区的修改撤销掉（unstage），重新放回工作区. 用HEAD时，表示最新的版本)

15. git rm (用于删除一个文件)

16. ssh-keygen -t rsa -C "youremail@example.com" (创建SSH Key)

17. git remote add origin git@github.com:Bruce333/other.git (关联github远程库)

18. git push -u origin master/git push origin master
    (推送到远程库,第一次用含有 -u 的命令,推送master分支的所有内容,此后用后面的命令推送最新修改)

19. git clone git@github.com:Bruce333/other.git (克隆一个本地库)

20. git checkout -b dev
    (创建dev分支，然后切换到dev分支,相当于以下两条命令:git branch dev[创建分支]/git checkout dev[切换分支])

21. git branch (列出所有分支，当前分支前面会标一个*号)

22. git checkout master (切换到master分支)

23. git merge dev (合并指定分支到当前分支)

24. git branch -d dev (删除dev分支)

25. git log --graph (查看分支合并图)

26. git merge --no-ff -m "merge with no-ff" dev
    (通常，合并分支时，如果可能，Git会用Fast forward模式，但这种模式下，删除分支后，会丢掉分支信息;--no-ff表示禁用Fast forward,用普通模式合并，合并后的历史有分支，能看出来曾经做过合并;-m参数，把commit描述写进去)

27. git stash (把当前工作现场“储藏”起来，等以后恢复现场后继续工作)

28. git stash list (查看工作现场) / git stash apply stash@{0} ()

29. git stash pop (恢复的同时把stash内容也删了,相当于:git stash apply[恢复]/git stash drop[删除])

30. git branch -D <name> (强行删除一个没有被合并过的分支)

31. git remote (查看远程库的信息) / git remote -v (显示更详细的信息)

32. git checkout -b branch-name origin/branch-name (在本地创建和远程分支对应的分支,本地和远程分支的名称最好一致)

33. 从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交

34. git pull
    (把最新的提交抓下来;如果提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，
    用命令git branch --set-upstream branch-name origin/branch-name)

35. git tag <name> <commit id 可无>
    (打一个新标签,默认标签是打在最新提交的commit上的;找到历史提交的commit id,可以给历史版本打标签)

36. git show <tagname> (查看标签信息)

37. git tag (查看所有标签)

38. git tag -a <tagname> -m "blablabla..." (指定标签信息)

39. git tag -s <tagname> -m "blablabla..." (用PGP签名标签)

40. git tag -d <name> (删除标签)

41. git push origin <tagname> (推送某个标签到远程)

42. git push origin --tags (一次性推送全部尚未推送到远程的本地标签)

43. git tag -d <tagname> (删除一个本地标签)

44. git push origin :refs/tags/<tagname> (删除一个远程标签)

45. git config --global color.ui true (让Git适当地显示不同的颜色)

46. 忽略某些文件时，需要编写.gitignore；.gitignore文件本身要放到版本库里，并且可以对.gitignore做版本管理

47. git config --global alias.st status
    (告诉Git，以后st就表示status,配置别名;加上--global是针对当前用户起作用的，如果不加，那只针对当前的仓库起作用;每个仓库的Git配置文件都放在.git/config文件中,别名就在[alias]后面，要删除别名，直接把对应的行删掉即可;而当前用户的Git配置文件放在用户主目录下的一个隐藏文件.gitconfig中)
