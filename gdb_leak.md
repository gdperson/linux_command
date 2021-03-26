   pmap -x pid  查看大块内存地址
   
   gdb 调试工具dump出可疑内存
   
   gdb, linux下强大的调试工具，但是我们不用它来调试，我们只用来输出内存的内容。即dump内存，前面用到的jmap dump只能看到jvm的内存信息，而gdb则可以看所有的，当然我们会用来看其他部分的内存。
   
   gdb attach <pid>                     先连接到进程中
  
   gdb dump memory /path/dump.bin 0x0011  0x0021    # dump 出内存段的信息,具体要 dump 的内存段地址，可以借助之前pmap 排查的结果,以及 cat /proc/<pid>/maps 中指示的地址段得出
  
   strings /path/dump.bin | less # 查看内存内容, 相信你能从中发现一些不一样的东西
