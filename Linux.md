## Linux



Linux相关

查看进程PID  

根据名称匹配：Ps -ef | grep xxxx

根据端口号 ： lsof -i:5000

关闭xxx的进程 ： kill -9 xxxx; 9：SIGKILL，强制中断一个进程的进行;

top 命令是Linux下常用的性能分析工具，能够实时显示系统中各个进程的资源占用状况，类似于Windows的任务管理器;

chmod命令, chown,chgrp

cat　用途是连接文件或标准输入并打印。这个命令常用来显示文件内容，或者将几个文件连接起来显示，或者从标准输入读取内容并显示.more,less，按页查看，前翻后翻。

tail: 从指定点开始将文件写到标准输出.使用tail命令的-f选项可以方便的查阅正在改变的日志文件,tail -f filename会把filename里最尾部的内容显示在屏幕上,并且不但刷新,使你看到最新的文件内容.

diff 命令用于比较两个文件或目录的不同

scp 命令是secure copy的简写，用于在Linux下进行远程拷贝文件的命令;

ssh远程登录；

ping; ifconfig

grep命令:该命令常用于分析一行的信息，若当中有我们所需要的信息，就将该行显示出来

grep -n '要查找的字符串'  被查的文件file:返回行数；

awk

cp复制，rm删除，mv移动，tar解压缩，mkdir，rmdir,