Here are the new instructions:

    sudo apt-get install coccinelle
    cd kernel
    make coccicheck MODE=report M=drivers/video/rockchip/bmp_helper.c 'SPFLAGS=--timeout 1' J=1

参考文档： Documentation/coccinelle.txt or Documentation/dev-tools/coccinelle.rst
