## Rethinking Multi-Instance Learning Through Graph-Driven Fusion: A Dual-Path Approach to Adaptive Representation

> data: 文本、网页、图像、医学四类共 24 个 MIL 数据集
>
> AAAI 2026 · [论文](https://doi.org/10.1609/aaai.v40i34.40081)

#### 引言

用软聚类压缩实例并学习动态稀疏图，再通过门控融合图特征与包级语义特征；属于跨任务的通用图 MIL 框架。

#### 方法

（1）ABMM：软聚类把包映射为更紧凑的表示。

（2）DGSL：以加权连接学习动态稀疏图。

（3）DPFF：门控融合图拓扑特征与保留的包语义。

##### 模型结构图

[![GDF-MIL 模型结构](../assest/GDF-MIL/figure-2-complete.webp)](../assest/GDF-MIL/figure-2-complete.webp)

图 2（PDF 第 3 页）

#### 实验

##### 实验设置

与 18 种方法比较；耗时采用五折、每折重复 100 次，统计每 epoch 平均时间。

##### 关键指标 { #key-results }

| 数据集 | ACC | F1 | AUC |
| --- | --- | --- | --- |
| News.aa | 0.940 ± 0.042 | 0.938 ± 0.043 | 0.937 ± 0.045 |
| News.cwx | 0.900 ± 0.035 | 0.895 ± 0.043 | 0.897 ± 0.048 |

数据来源为原文表 1，PDF 第 5 页，文本 MIL 五折验证。

##### 结果解读

文本基准中，图结构与多尺度特征融合在不同数据集上的收益并不相同。ABMIL 训练更快，使用图构建时需要同时比较性能和开销。

##### 消融与讨论

消融软聚类映射、动态图与双路门控，考察表征质量和图构建效率的折中。

#### 参考文献

> Rethinking Multi-Instance Learning Through Graph-Driven Fusion: A Dual-Path Approach to Adaptive Representation
>
> AAAI 2026 · [论文](https://doi.org/10.1609/aaai.v40i34.40081)

本文归入相关 MIL 方法：具体研究对象见数据与实验设置。
