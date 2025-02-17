# Friedkin-Johnsen 观点演化模型
该代码实现了一个 Friedkin-Johnsen (FJ) 模型，用于模拟有向图中节点观点的动态演化过程。模型通过迭代更新节点的表达观点，最终达到平衡状态。

## Table of contents

* [我的环境](#我的环境)
* [代码结构](#代码结构)

## 我的环境

* Python 3.9.6
* Numpy 2.0.2
* Networkx 3.2.1


## 代码结构
### FJeasy.py
手动实现了FJ模型，包括以下几部分：
* 定义图结构：支持3节点有向图的邻接矩阵配置（此处链式结构 0→1→2）
* 内部观点生成：随机生成节点的初始内部观点（区间 [0,1)）
* 初始化表达观点，与内部观点相等
* 迭代更新机制：通过多轮迭代更新表达观点（此处迭代次数为5次）


