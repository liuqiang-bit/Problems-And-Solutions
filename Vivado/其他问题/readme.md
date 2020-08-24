# 其他问题

GitHub地址：https://github.com/liuqiang-bit/Problems-And-Solutions.git

### 一、M_GPx_AXI_ACLK时钟频率导致某些模块不运行

作者：GUDONG		时间：2020/08/24		软件：Vivado 2018.3

​		下图中M_GP0_AXI_ACLK连接在FCLK_CLK1(150MHz)时钟上时stream2mem_0模块在SDK中能成功配置并下载，但此模块无法运行，连接到FCLK_CLK0(100MHz)时无问题。

![](F:\MyGit\Problems-And-Solutions\Vivado\其他问题\images\1.png)

> ​		最省事的办法是把所有M_AXI_GPx_ACLK和S_AXI_GP0_ACLK连到同一个时钟上。