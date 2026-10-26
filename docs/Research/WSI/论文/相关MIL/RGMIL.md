## Reinforced GNNs for Multiple Instance Learning

> data: 五个经典 MIL 基准、五个新闻文本数据、三个医学图像数据
>
> IEEE Transactions on Neural Networks and Learning Systems 2025 · [论文](https://doi.org/10.1109/TNNLS.2024.3392575) · [作者代码](https://github.com/RingBDStack/RGMIL)

#### 引言

使用多智能体强化学习同步调整包内图结构和图神经网络架构，学习两者的关联，减少图构建与网络选择分离带来的限制。

#### 方法

（1）图状态：将包内实例关系和网络配置作为联合优化对象。

（2）多智能体决策：分别调整边结构和 GNN 架构，保留相互依赖。

（3）强化反馈：以任务表现评价策略，使构图与信息聚合协同搜索。

#### 实验

##### 实验设置

同时评估包分类和图结构/网络架构选择，比较浅层 MIL 与深度图模型。

##### 主要结果

经典五个数据集上 RGMIL 的 ACC 均领先比较基线；支持的是特定图结构与网络架构联合搜索的有效性。

##### 消融与讨论

分析边过滤阈值与 GNN 层数的协同关系，不把强化学习搜索收益等同于单纯加深网络。

#### 参考文献

> Reinforced GNNs for Multiple Instance Learning
>
> IEEE Transactions on Neural Networks and Learning Systems 2025 · [论文](https://doi.org/10.1109/TNNLS.2024.3392575) · [作者代码](https://github.com/RingBDStack/RGMIL)

本文归入相关 MIL 方法：具体研究对象见数据与实验设置。
