#命令行进行时钟的操作

##依赖:

kernel 4.4:
需打开: CONFIG_ROCKCHIP_PM_TEST

##使用说明:

    cat /sys/pm_tests/clk_rate

    get clk rate:
             echo get [clk_name] > /sys/pm_tests/clk_rate
    set clk rate:
             echo rawset [clk_name] [rate(Hz)] > /sys/pm_tests/clk_rate
    enable clk:
             echo open [clk_name] > /sys/pm_tests/clk_rate
    disable clk:
             echo close [clk_name] > /sys/pm_tests/clk_rate
