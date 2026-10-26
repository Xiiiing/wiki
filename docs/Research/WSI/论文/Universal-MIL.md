## A Universal Multiple Instance Learning Framework for Whole Slide Image Analysis

> data: CAMELYON16、TCGA-NSCLC、SICAPv2、PANDA；MUSK1/2、Fox、Tiger、Elephant
>
> Computers in Biology and Medicine 2024 · [论文](https://doi.org/10.1016/j.compbiomed.2024.108714)

#### 引言

联合实例标准化、深层投影、自注意力和实例伪标签评价进行聚合，再用关键实例选择强化局部特征，服务弱监督切片分类。

#### 方法

（1）实例标准化：调整特征分布并通过深层投影增强可分性。

（2）关系与伪标签：自注意力学习依赖，并以实例级评价补充弱监督。

（3）关键实例选择：在初步包预测外加强局部证据，再组合最终结果。

#### 实验

##### 实验设置

同时检查 WSI 分类与经典 MIL 向量数据；不同任务中是否需要特征编码器不同。

##### 主要结果

实验分别比较聚合模块与关键实例选择；经典向量数据上的结果只能支持聚合泛化。

##### 消融与讨论

考察标准化、自注意力、伪标签评价及关键实例选择；整体结果需区分第一阶段和增强预测阶段。

#### 参考文献

> A Universal Multiple Instance Learning Framework for Whole Slide Image Analysis
>
> Computers in Biology and Medicine 2024 · [论文](https://doi.org/10.1016/j.compbiomed.2024.108714)
