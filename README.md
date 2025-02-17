# Friedkin-Johnsen 观点演化模型
该代码实现了一个 Friedkin-Johnsen (FJ) 模型，用于模拟有向图中节点观点的动态演化过程。模型通过迭代更新节点的表达观点，最终达到平衡状态。

## Table of contents

* [我的环境](#我的环境)
* [代码结构](#代码结构)
* [如何运行](#如何运行)

## 我的环境

* Python 3.9.6
* Numpy 2.0.2
* Networkx 3.2.1
* matplotlib 3.9.4


## 代码结构
### FJeasy.py
手动实现了FJ模型，包括以下几部分：
* 定义图结构：支持3节点有向图的邻接矩阵配置（此处链式结构 0→1→2）
* 内部观点生成：随机生成节点的初始内部观点（区间 [0,1)）
* 初始化表达观点：与内部观点相等
* 迭代更新机制：通过多轮迭代更新表达观点（此处迭代次数为5次）  

在实现了FJmodel.py之后，在此处调用检查，结果相同。

### FJmodel.py
包含了Friedkin-Johnsen模型的核心实现。定义了一个 FJModel 类，该类初始化模型并提供了迭代计算表达观点平衡状态的方法。 主要功能包括：
* 初始化模型：接受邻接矩阵和可选的内部观点向量。
* 迭代计算：通过迭代更新表达观点，直到达到最大迭代次数或满足收敛条件。
* 收敛检查：可选参数，用于提前结束迭代。

### 如何运行
运行 python FJeasy.py 来执行示例。