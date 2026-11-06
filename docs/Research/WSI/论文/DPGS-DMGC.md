## Distributed Parallel Gradient Stacking(DPGS): Solving Whole Slide Image Stacking Challenge in Multi-Instance Learning

> data: CAMELYON16 多尺度/ImageNet 特征、TCGA-Lung 多尺度/UNI2 特征
>
> ICML 2025 · [论文](https://proceedings.mlr.press/v267/wu25ae.html)

#### 引言

面向实例数不一致导致的 MIL 批次堆叠难题，结合分布式梯度堆叠与模型、梯度压缩，提高训练效率并降低通信开销。

#### 方法

（1）梯度堆叠：在保留不同长度包信息的同时组织并行计算。

（2）分布式管理：协调多个工作模型的梯度与参数更新。

（3）DMGC：压缩模型和梯度通信，降低分布式训练开销。

##### 模型结构图

[![DPGS / DMGC 模型结构](assest/DPGS-DMGC/figure-2-complete.webp)](assest/DPGS-DMGC/figure-2-complete.webp)

图 2（PDF 第 3 页）

#### 实验

##### 实验设置

比较原始训练、padding、固定采样与 DPGS；同时记录 ACC、收敛时间和通信开销。

##### 关键指标 { #key-results }

| ABMIL 设置 | ACC（%） | 收敛耗时（秒） |
| --- | --- | --- |
| 基线 | 92.38 ± 0.23 | 636.3 ± 12.7 |
| 加入 DPGS + DMGC | 93.90 ± 0.13 | 20.0 ± 2.4 |

数据来源为原文表 2，PDF 第 6 页，TCGA-Lung 多尺度特征，批大小 32。

##### 结果解读

TCGA-Lung 上 ABMIL 的 ACC 从 92.38% 到 93.90%，收敛时间从 636.3s 到 20.0s；该加速属于对应实现与硬件设置。

##### 消融与讨论

单独检查 DPGS 堆叠和 DMGC 压缩，区分数据使用方式、训练并行性与压缩近似带来的变化。

#### 参考文献

> Distributed Parallel Gradient Stacking(DPGS): Solving Whole Slide Image Stacking Challenge in Multi-Instance Learning
>
> ICML 2025 · [论文](https://proceedings.mlr.press/v267/wu25ae.html)
