# 其他问题

GitHub地址：https://github.com/liuqiang-bit/Problems-And-Solutions.git

### 一、LWIP库不能通过修改system.mss更新配置

作者：GUDONG		时间：2020/08/24		软件：Vivado SDK 2018.3

​		必须在建立bsp时配置好LWIP库，否则通过修改system.mss再Generate bsp不会更新库配置。