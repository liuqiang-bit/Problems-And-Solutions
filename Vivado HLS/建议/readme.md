# 一些使用HLS的建议

GitHub地址：https://github.com/liuqiang-bit/Problems-And-Solutions.git

作者：GUDONG		时间：2020/08/27		软件：Vivado HLS 2018.3

## 一、提升综合速度

1.使用ap_fixed类型取代float和double

​		将https://github.com/liuqiang-bit/SURF_HLS_Simplified.git工程中float型SurfHB变量换成ap_fixed型,原本需要近1小时的综合时间减少到只需几分钟。

![](F:\MyGit\Problems-And-Solutions\Vivado HLS\建议\images\1.png)

## 一、减少资源占用

1.使用ap_fixed类型取代float和double

​		将https://github.com/liuqiang-bit/SURF_HLS_Simplified.git工程中float型SurfHB变量换成ap_fixed型对比效果