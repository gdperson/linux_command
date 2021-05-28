yum install -y dstat。dstat -tnf 1 10 输出接下来10秒内每秒的网络数据

sar 命令来自 sysstat 包，可使用这个命令安装：yum install -y sysstat。sar -n TCP 1 10可查看接下来10秒内的tcp数据
