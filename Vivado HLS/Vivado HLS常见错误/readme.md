# Vivado HLS 常见错误

GitHub地址：https://github.com/liuqiang-bit/Problems-And-Solutions.git

[TOC]

## 一、综合时报错，memcpy未定义

作者：GUDONG		时间：2020/09/06		软件：Vivado HLS 2018.3

### 1.问题描述

使用memcpy后，C仿真没问题，但是综合时报错：error: use of undeclared identifier 'memcpy'

### 2.解决措施

包含string.h

## 二、联合仿真时报错，DEADLOCK DETECTED。

作者：GUDONG		时间：2020/09/10		软件：Vivado HLS 2018.3

### 1.问题描述

数据通过hls::stream对象在函数间传递数据，但联合仿真时报错，DEADLOCK DETECTED，导致仿真停止，如下图所示。

![](F:\MyGit\Problems-And-Solutions\Vivado HLS\Vivado HLS常见错误\images\1.png)

### 2.解决措施

使用STREAM指令给hls::stream对象指定足够的深度。

## 三、ERROR [XFORM 203-801]

作者：GUDONG		时间：2020/09/10		软件：Vivado HLS 2018.3

### 1.问题描述

一个m_axi接口作为两个函数的参数导致综合时报错，接口冲突

<img src="F:\MyGit\Problems-And-Solutions\Vivado HLS\Vivado HLS常见错误\images\2.png"  />

![](F:\MyGit\Problems-And-Solutions\Vivado HLS\Vivado HLS常见错误\images\3.png)

### 2.解决措施

将读和谐操作使用不同的m_axi接口。

<img src="F:\MyGit\Problems-And-Solutions\Vivado HLS\Vivado HLS常见错误\images\4.png" style="zoom: 50%;" />

<img src="F:\MyGit\Problems-And-Solutions\Vivado HLS\Vivado HLS常见错误\images\5.png" style="zoom: 50%;" />

