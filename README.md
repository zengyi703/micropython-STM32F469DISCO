micropython for STM32F469DISCO board!

进入到stm32目录，然后make就可以生成烧写文件
cd ports/stm32
make

将文件烧写到STM32F469开发板中即可
1.已经调好了SDRAM，micropython可能使用的RAM达16MByte。
2.插入tfcard，可以支持，如果不插入tf卡，可跟官方一样用内部flash虚拟成U盘。

开机命令如下所示：
MicroPython v1.9.4-631-g338635c-dirty on 2018-11-09; F469I-DISCO with STM32F469
Type "help()" for more information.
>>> import micropython
>>> micropython.mem_info()
stack: 492 out of 80896
GC: total: 16392960, used: 1248, free: 16391712
 No. of 1-blocks: 13, 2-blocks: 8, max blk sz: 40, max free sz: 1024470
>>>