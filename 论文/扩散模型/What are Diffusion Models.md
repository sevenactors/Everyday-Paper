论文名称：What are Diffusion Models?

地址：[What are Diffusion Models? | Lil'Log](https://lilianweng.github.io/posts/2021-07-11-diffusion-models/)

​		   [由浅入深了解Diffusion Model - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/525106459)

发表：博客

日期：2023/5/24

=======

【summary】

本文是一篇介绍Diffusion Model的博客，分三部分介绍：Diffusion前向过程、Diffusion逆向过程以及Diffusion训练。Diffusion Model是一个加噪与去噪的过程，在前向过程中，Diffusion Model对原始图片不断地加入小的高斯噪声；在逆向过程中，Diffusion Model对加噪后的结果一步步地进行去噪。加噪一般是固定过程，模型被训练用于去噪。

【points】

1. 重参数技巧（reparameterization trick）：使得高斯采样过程也能保持梯度传递

2. 加噪过程一步到t：由于独立同分布的高斯噪声的加和仍为高斯噪声，因此能够一步迭代到t步的加噪结果

3. 逆向条件概率公式的推导：巧妙地建立了xt与xt-1的关系

4. 模型前向过程：根据xt与t预测噪声（参数所在），之后用固定公式计算出均值方差，最后用重参数采样出xt-1

   ![Diffusion Model前向过程](D:\GitHub工程\Everyday-Paper\论文\img\WADM1.png)

5. loss的推导

6. 整个算法步骤：

   ![Diffusion Model算法流程伪代码](C:\Users\管理员\AppData\Roaming\Typora\typora-user-images\image-20230525111912455.png)

【unknown】

本文的“加速Diffusion采样和方差的选择(DDIM)”还没看，等理解了基础模型之后再来详细了解
