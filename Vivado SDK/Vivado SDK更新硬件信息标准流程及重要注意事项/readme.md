# Vivado SDK更新硬件信息标准流程及重要注意事项

GitHub地址：https://github.com/liuqiang-bit/Problems-And-Solutions.git

作者：GUDONG		时间：2020/08/15		软件：Vivado 2018.3、Vivado SDK 2018.3

------

> **目录**

[TOC]

------

### 1.Generate Output Product

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\1.png" style="zoom:50%;" />

### 2.Create HDL Wrapper

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\2.png" style="zoom:50%;" />

### 3.run Synthesis

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\3.png" style="zoom:50%;" />

### 4.run Implimentation

> ​		**此过程很重要，可以知道时序是否和要求，以及资源使用量若。有时SDK不导入硬件信息也是由于时序不合要求。

​		Synthesis结束后弹出此框进行Implimentation

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\4.png" style="zoom:50%;" />

​		或者

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\5.png" style="zoom:50%;" />

### 5.Generate Bitstream

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\6.png" style="zoom:50%;" />

### 6.Export Hardware

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\7.png" style="zoom:50%;" />

### 7.Launch SDK

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\8.png" style="zoom:50%;" />

### 8.Refresh bsp

> bsp的libsrc文件夹下的驱动最好别手动删除，例如有时候在Vivado中移除了某些IP，但是启动SDK并Refresh后libsrc目录下还有这些IP的驱动文件夹，别手动删除这些文件夹，极有可能导致第三方库文件完全无法识别，库文件无法识别后只能新建Application配置第三方库才能解决。

<img src="F:\MyGit\Problems-And-Solutions\Vivado SDK\Vivado SDK更新硬件信息标准流程及重要注意事项\images\9.png" style="zoom:50%;" />