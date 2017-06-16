### 安装GIT
 使用下面的命令进行安装git工具. 
 
 sudo apt-get install git 
### 创建版本库
  什么是版本库呢？版本库又名仓库，英文名repository，你可以简单理解成一个目录，这个目录里面的所有文件都可以被Git管理起来，每个文件的修改、删除，Git都能
跟踪，以便任何时刻都可以追踪历史，或者在将来某个时刻可以“还原”。

第一步, 先要创建一个目录, 这个目录就是用来存放仓库的.

$ mkdir html
$ cd html

第二步, 使用git init命令, 将当前目录创建成git仓库.

$ git init
Initialized empty Git repository in /home/user/html/.git/

马上就把仓库创建成功了, 并提示这是一个空仓库.

$ ls -al

.git
### 增加文件
1. 创建一个文件README.
```
$ touch README
```
2. 编辑这个文件, 写一点东西在里面.
```
$ vim README
```
3. 先用查看当前状态的命令, 查看一下现在目录下文件的状态.
```
$ git status
```
4. 把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化.
```
$ git add README
```
5. 现在使用查看状态的命令, 看一下是目录下文件的状态.
```
$ git status
```
### 配置用户信息
配置用户名, 这个用户名是你的提交patch的名字
```
$ git config --global user.name
```
配置用户邮箱
```
$ git config --global user.email
```
配置编辑提交信息的编辑器, 我们熟悉的编辑器是vim.
```
$ git config --global core.editor vim
```
### 提交
```
$ git commit
```
### 查看提交信息
```
$ git log
```
