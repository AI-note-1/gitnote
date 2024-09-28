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
