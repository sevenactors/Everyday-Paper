论文名称：Integral Neural Networks

地址：[论文地址](https://openaccess.thecvf.com/content/CVPR2023/papers/Solodskikh_Integral_Neural_Networks_CVPR_2023_paper.pdf)

发表：CVPR 2023 Award Candidates

日期：2023/5/23

分类：理论

=======

【summary】

本文介绍了一种使用连续函数的积分作为基本算子的神经网络架构，称之为积分神经网络（INN）。区别于传统的离散形式神经网络(DNN）使用标量与向量，积分神经网络使用函数代表输入、输出以及参数，使用函数乘积的积分作为网络前向传播的过程。  

借助函数离散化的技术，研究者发现能够将INN离散化成DNN，而通过控制离散的程度（即函数近似时取点的步长），INN能够离散化成任意参数量大小的DNN，从而能够在部署到边缘设备时控制内存量与计算量。

【ideas】

