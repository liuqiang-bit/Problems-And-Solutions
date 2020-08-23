# ERROR [BD 41-703]解决办法

GitHub地址：https://github.com/liuqiang-bit/Problems-And-Solutions.git

作者：GUDONG		时间：2020/08/15		软件：Vivado 2018.3

### 错误描述

ERROR: [BD 41-703] 

### 错误产生的原因

​		手动调整HP端口的数据源端口，如下两图所示。

​		原始连接如下。

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\1.png)

​		调整后如下。

<img src="F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\2.png"  />

3.Generate Output Products后报此错误。意思是axi_vdma_0的S2MM端口地址没有映射到HP0端口，stream2mem_0的m_axi_pMemPort端口没有映射到HP1。

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\3.png)

4.点击Adress Editor

​		发现此时两个模块还是绑定的之前的地址，现在要交换地址，但正好被彼此占用了，所以绑定不了。

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\4.png)

6.Unmap Segment接触之前的绑定。

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\5.png)

7.点击Auto Assign Address

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\6.png)

​		绑定成功。

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\7.png)

8.Generate Output Product

​		无错误。

![](F:\MyGit\Problems-And-Solutions\Vivado\ERROR[BD 41-703]\images\8.png)