# android simpleperf

perf是linux上非常好用的性能调试工具，可以监测各种事件, simpleperf是perf的精简版，
但也足够使用。

android 7.1工程里面默认带了simpleperf工具.

使用方法:

    //打开内核符号表
    echo 0 >/proc/sys/kernel/kptr_restrict
    //记录cpu函数调用耗时
    simpleperf record -g `pgrep surface`
    带调用栈的报告
    simpleperf report -g

通过simpleperf report, 可以快速找到cpu热点函数
