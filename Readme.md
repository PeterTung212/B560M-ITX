硬件配置：

显卡：Onda RX560 典范 4G DDR5

CPU：i9 10900ES（QTB1）

主板：ASrock B560M-ITX-AC

硬盘：雷克沙（Lexar）NM700 1TB

电源：益衡Flex 7660B 400W

无线网卡和蓝牙：DW1560 BCM94352Z

内存：海盗船 16GB 3200 DDR4 x2

步骤：

1、Windows环境使用DiskGenius在U盘建立ESP（EFI 300M）、MSR（16M）分区

2、使用Diskpart将EFI分区设置为可读/写

  2.1）ist disk          （列出磁盘）
  
  2.2）sele disk 0       （0为选择的磁盘号）
  
  2.3) list part          (列出分区）
  
  2.4) sele part 1      （选择第一分区）
  
  2.5) set id=ebd0a0a2-b9e5-4433-87c0-68b6b72699c7   （把分区id 改为系统能识别的id ，不影响使用）
  
  2.6) assign letter=x     (x为分配的盘符）
  
  U盘此时可通过x：进行操作，如果系统显示权限不够请重启后操作
  
3、将下载的EFI文件夹拷贝至EFI分区根目录下

（待续......）
