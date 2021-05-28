yum install -y dstat。dstat -tnf 1 10 输出接下来10秒内每秒的网络数据

sar 命令来自 sysstat 包，可使用这个命令安装：yum install -y sysstat。sar -n TCP 1 10可查看接下来10秒内的tcp数据

ss 和 netstat 是查看活动链接/监听端口的常用命令。ss 是 netstat 的替代，性能更好，建议使用。

ss 是 iproute2util 包的一部分，因此在大多数系统上默认安装，也可通过yum install -y iproute安装。netstat 来自 net-tools 包，新版系统上需要自行安装：yum install -y net-tools
ss -nt 查看 tcp 链接
