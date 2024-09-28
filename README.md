
 # Git使用方式：
 1. 首先用 cd /d 进入d盘
 2. mkdir <file> 在d盘上建立一个新的文件夹
 3. cd <file> 进入该文件夹
 4. git init 命令将该文件夹变成git管理的版本库
 5. 在使用git add 命令之前，必须先在该文件夹下建立文件
 有两种方法：
 - 1.在 git上使用touch 命令直接创建文件 **touch是linux的命令，可以直接创建一个文件**
 - 2.使用 vi/vim 命令创建文件，可以直接写内容，按下 i 进入输入模式，按下 esc 退出输入，按下 shift+: wq 保存内容返回 git bash **VIM/VI是linux里面命令行下的代码编辑器，可以用来创建修改代码**
 6. 使用git add file 提交到暂存区
 7. git commit -m "注释"

 # 对分支和文件操作:

  ## git status 的使用:
  1. 在有一个本地库的前提下，再使用 vi 创建一个新文件，git status 会显示Untracked file
  2. 使用 git add 后会出现 Changes not staged for commit
  3. 使用 git commit 后会出现 no changes added to commit

  ## git pull & git push:
  1. 要想将github 中最新的版本拉取到本地进行操作，先 git pull origin master
  2. 将更改的文件 push 到github 上则会出现 **冲突**，要先解决冲突
  3. 使用 cat 命令查看不同 ，再使用 vi 去修改保留你所需要的内容
  4. 再 git add ,git commit -m ""
  5. 最后 git push origin master

  ## git log & git reset --hard 
  1. 使用 git log 可以查看所有版本的 **版本号和注释**
  2. git log --pretty=oneline 可以只查看 版本号
  3. 在git中，head指向当前版本，head^ 指向上一版本
  4. 可以使用 git reset --hard head^ 回到上一版本，或者直接 --hard 版本号回到任意版本，最新版本的版本号可以到上面 git log 命令找
  5. 若将git 关闭了，可以使用 git relog 查看之前的所有命令

  ## 工作区和暂存区
   使用 vi 新建修改文件后，使用git add 就将文件放到暂存区中，等所有文件操作完毕后，使用 git commit -m 统一提交

  ## git diff
   git diff HEAD -- 文件名就可以查看工作区和版本库里面最新版本的区别

  ## 撤销修改
  1. 错误的文件还在工作区，没被提交到暂存区，则直接使用 git checkout -- file,将file丢去,回到最近的版本，注意：**必须要有 -- ，否则就是切换到另一分支的命令**
  2. 错误的文件已经提交到暂存区，但还没有 commit,可以使用 git reset HEAD <file>回到第一步，在进行第一步的操作，注意与**git reset --hard 版本** 版本回退有区别
  3. 若已经 commit，则使用版本回退重新写，前提：**未推送到远程库**

  ## delete file
  1. git rm <file>删除文件
  2. 若是将已经提交到版本库中的文件删除，可使用 git checkout -- file 恢复到最近的版本

 # 远程仓库
  ## 将本地库推送到远程库
  1. 第一次推送 git remote add origin 仓库地址，origin 为远程库名，可以改变，但>下次 push 的时候名字也要变
  2. 后面将新版本推送 git push origin master

  ## clone
  1. 先在本地创建一个新的文件夹
  2. cd 该文件夹
  3. git clone 仓库地址，就将代码 fork到该文件夹
