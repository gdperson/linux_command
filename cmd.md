who -b 查看最后一次系统启动的时间。

who -r 查看当前系统运行时间

last reboot

可以先用 top 命令查看指定进程（xxx）的CPU占用率是否异常，命令如下：

top -p `ps aux | grep "xxx" | grep -v grep | cut -c 9-15`

perf record -a -g -F 99 -p 21212

flamegraph火焰图

1、第一步

$sudo perf record -e cpu-clock -g -p 28591

Ctrl+c结束执行后，在当前目录下会生成采样数据perf.data.

2、第二步

用perf script工具对perf.data进行解析

perf script -i perf.data &> perf.unfold

3、第三步

将perf.unfold中的符号进行折叠：

#./stackcollapse-perf.pl perf.unfold &> perf.folded

4、最后生成svg图：

./flamegraph.pl perf.folded > perf.svg

pstack pid //进程调用堆栈
strace -p pid //进程系统调用
perf top -p pid //进程实时调用函数情况
perf stat -p pid //运行命令会挂载,ctr+c 后显示统计调用系统 cpu 使用时间等
sudo perf trace -p pid //当前程序系统调用函数显示
sudo perf ftrace -p pid //当前程序系统内核调用时间情况

sudo tcpdump -vv -i interface port 6379
