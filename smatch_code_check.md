Here are the new instructions:

    git clone git://repo.or.cz/smatch.git
    cd smatch
    make
    cd ~/your/code/
    make clean
    make CHECK="~/path/to/smatch/smatch --full-path" \
                CC=~/path/to/smatch/cgcc | tee warns.txt
Except if you are using smatch against the kernel the command is:

    make CHECK="~/path/to/smatch/smatch -p=kernel" C=1 \
                bzImage modules | tee warns.txt

参考文档： http://smatch.sourceforge.net/
