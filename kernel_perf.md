# 编译：

rk3399 kernel 4.4:

    cd kernel/tools/perf
    make LDFLAGS=-static ARCH=aarch64 CROSS_COMPILE=aarch64-linux-gnu- 

使用:

    打开内核符号表
    echo 0 > /proc/sys/kernel/kptr_restrict
    精简的报告，可以快速看到哪个函数占用最高
    perf record `pgrep xxx(你的程序)`
    perf report > simple_report.txt
    带调用栈，结合simple_report.txt， 找到热点函数的调用栈
    perf record -g `pgrep xxx(你的程序)`
    perf report > stack_report.txt
