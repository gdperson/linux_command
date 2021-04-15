who -b 查看最后一次系统启动的时间。

who -r 查看当前系统运行时间

last reboot

可以先用 top 命令查看指定进程（xxx）的CPU占用率是否异常，命令如下：

top -p `ps aux | grep "xxx" | grep -v grep | cut -c 9-15`
