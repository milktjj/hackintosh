# hackintosh
（hackintosh) 

>>电脑配置信息

配件  |  型号
------|-------------------
CPU   | AMD Ryzen R5 2600
GPU   | AMD Rx Vega 56
MOBO  | Gigabyte X470

# 1. 制作启动盘 

>>来自AMD OSX论坛 amd highsierra V2.5
使用transmac软件
1. 选中U盘，格式化为apple的格式
2. restore from imgae 
3. 使用disk genius挂载EFI分区，选择合适的kext

# 2. 安装

## 2.1 第一次启动

第一次启动选择从启动盘进入，选择磁盘工具，格式化为apple的文件格式

## 2.2 第二次启动

第二次启动选择从启动盘进入，选择终端，使用xlnc命令进行内核、驱动配置，完成后重启

## 2.3 第三次启动  

第三次启动从安装盘进入，完成最后的安装和配置

**安装中遇到的问题：**
1. 格式化时提示失败，磁盘空间不足---------解决方法：因为apple的需要EFI分区大于200M，用于存放日志文件系统的信息（可能），重新格式化，建立大于200M的EFI分区，或者使用disk genius压缩windwos恢复分区，将空出的空间给到EFI上。

>>至此为止，基本的系统安装已经完成

# 3. 解决小问题
## 3.1 关机、重启不断电
利用dsdt使用苹果原生的USB驱动 [具体方法](https://amd-osx.com/forum/viewtopic.php?t=4986)
## 3.2 声音没有
下载AppleALC.kext，layoutid设为11






