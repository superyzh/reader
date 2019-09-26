
# create a new repository on the command line
## git init
## git add README.md
## git commit -m "first commit"
## git remote add origin https://github.com/superyzh/reader.git
## git push -u origin master

#  push an existing repository from the command line
## git remote add origin https://github.com/superyzh/reader.git
## git push -u origin maste

#从远程分支拉取代码到本地  
## git pull https://github.com/superyzh/reader  master  


# git commit、git push、git pull、 git fetch、git merge 的含义与区别

## git commit：是将本地修改过的文件提交到本地库中；
## git push：是将本地库中的最新信息发送给远程库；
## git pull：是从远程获取最新版本到本地，并自动merge；
## git fetch：是从远程获取最新版本到本地，不会自动merge；
## git merge：是用于从指定的commit(s)合并到当前分支，用来合并两个分支；
