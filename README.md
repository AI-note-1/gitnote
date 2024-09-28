 首先用 cd /d 进入d盘

 mkdir <file> 在d盘上建立一个新的文件夹

 cd <file> 进入该文件夹

 git init 命令将该文件夹变成git管理的版本库

 在使用git add 命令之前，必须先在该文件夹下建立文件

 有两种方法：1.在 git上使用touch 命令直接创建文件

 2.使用 vi/vim 命令创建文件，可以直接写内容，按下 i 进入输入模式，按下 esc 退出输入，按下 shift+: wq 保存内容返回 git bash

 使用git add file 提交到暂存区

 git commit -m "注释"

#对分支和文件操作
##git status 的使用
1.在有一个本地库的前提下，再使用 vi 创建一个新文件，git status 会显示Untracked file
2.使用 git add 后会出现 Changes not staged for commit
3.使用 git commit 后会出现 no changes added to commit
