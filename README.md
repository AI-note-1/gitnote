
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
  2. 此时将更改的文件 push 到github 上则会出现 **冲突**，要先解决冲突
  3. 使用 cat 命令查看不同 ，再使用 vi 去修改保留你所需要的内容
  4. 再 git add ,git commit -m ""
  5. 最后 git push origin master
