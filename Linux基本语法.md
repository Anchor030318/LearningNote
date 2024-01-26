### ls查看文件
- ls 查看目录下所有文件
- ls -a 可以查询被隐藏的文件
- ls -l 查看文件的详细信息

### cd切换目录
- cd /接绝对路径
- cd. 从当前目录开始接相对路径
- cd.. 从上一级目录开始接相对路径

### mkdir创建文件夹
- mkdir +文件夹名称（相对或者绝对路径）
- mkdir a1 在当前文件夹中创建a1文件夹
- mkdir -p a1/b1 创建b1文件夹，若a1文件夹不存在则一并创建

### touch创建空白文件
- touch whw.txt 创建一个空白的whw.txt文件

### echo打印
- echo hello 向控制台打印hello字符串

### >/>>指定输出的文件
- echo hello > 1.txt 向1.txt文件中输出hello
- >:覆盖文件原有内容
- >>:在文件中追加新内容

### cat查看文件内容
- cat 1.txt 在控制台打印1.txt文件中的内容

### cp 复制

### mv移动和重命名

### rm 删除
- -f 不带询问的删除
- rm -f 文件名 直接删除文件，不询问
- rm -rf 文件夹 直接删除文件夹，不询问

### pwd打印当前所在的目录路径

### more less head tail
- more和less：分页展示文件中的内容
	- more；只能下翻
	- less：可以利用键盘上下键进行上下翻，q键退出查看
- head：查看文件的前n行 head -n 5
- tail：查看文件的最后几行；还可以查看日志文件，监听文件，打印出新产生的日志信息
### tab自动补全命令、文件路径等

### grep 根据关键字查找

### find从系统中进行查找

### systemctl 系统服务
- 开启：systemctl start 服务名
- 关闭：systemctl stop 服务名

### ps -ef 查看虚拟机正在运行的进程

### kill -9 进程id

### tar 对文件进行压缩和解压缩操作

