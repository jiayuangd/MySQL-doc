
# ubuntu
下载ubuntu在虚拟机中安装，安装VMware-tools，安装VIM，git,然后配置VIM，装入输入法。
# Linux 操作系统组成
一个典型的Linux操作系统组成为：Linux内核，一些GNU程序库和工具，命令行shell，图形界面的X Window系统和相应的桌面环境，如KDE或GNOME，并包含数千种从办公套件，编译器，文本编辑器到科学工具的应用软件。

Shell俗称壳（用来区别于核），是指“提供使用者使用界面”的软件（命令解析器）。它类似于DOS下的command和后来的cmd.exe。它接收用户命令，然后调用相应的应用程序，并根据用户输入的指令来反馈给用户指定的信息。
# 文本编辑器Vim的基本使用
## Vim介绍
Vim是一个类似于Vi的著名的功能强大、高度可定制的文本编辑器，在Vi的基础上改进和增加了很多特性。Vim是纯粹的自由软件在代码补全、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用，和Emacs并列成为类Unix系统用户最喜欢的文本编辑器。
## Vim的基本使用
1. i：在当前字符的左边插入
1. I：在当前行首插入
1. a：在当前字符的右边插入
1. A：在当前行尾插入
1. o：在当前行下面插入一个新行
1. O：在当前行上面插入一个新
1. h: 向前移动一个字符
1. j: 向上移动一行
1. k: 向下移动一行
1. l: 向后移动一个字符
1. yy: 复制当前一行
1. dd:剪切当前一行
1. p: 粘贴内容到游标之后
1. P: 粘贴内容到游标之前

# Linux文件系统介绍

文件系统是操作系统用于明确存储设备或分区上的文件的方法和数据结构；即在存储设备上组织文件的方法。

## Linux文件系统分类

- 磁盘文件系统：指本地主机中实际可以访问到的文件系统，比如磁盘。
- 网络文件系统：是可以远程访问的文件系统，这种文件系统在服务器端仍是本地的磁盘文件系统，客户机通过网络远程访问数据，比如NFS。
- 专有/虚拟文件系统：不驻留在磁盘上的文件系统，比如proc，sys等。

## Linux文件系统结构
![Image of Yaktocat](https://nts.newbieol.com/static/k6/mySQL/class-002/img/linux_fs.jpg)

# 基本的文件操作

* 文件的创建、删除、复制、重命名、移动
```
touch  file
cp file file1
cp file  /home/linux/file1
mv file   file2
mv file  /home/linux/
```
* 列出文件列表
ls -al  .
* 查看文件内容
cat  file
# 基本的目录操作
* 目录的创建、删除、复制、重命名、移动
```
mkdir dir
cp dir   dir1  -a
cp dir   /home/linux/dir2  -a
mv dir  dir2
mv dir  /home/linux/
rm  dir  -rf
```
* 列出目录列表
ls -d  dir 
* 目录中查找文件
find  ./dir  -name  "filename"
# 文件的归档和压缩
* 使用gzip和gunzip对文件进行压缩和解压缩
* 使用bzip2和bunzip2对文件进行压缩和解压缩
* 使用tar对文件和目录进行压缩和解压缩
```
gzip  filename
bzip2  filename
gunzip filename
bunzip2  filename
tar czvf  file.tar.gz dir
tar cjvf  file.tar.bz2 dir
tar cJvf  file.tar.xz  dir
tar xvf  file.tar.gz
tar xvf  file.tar.xz
```

