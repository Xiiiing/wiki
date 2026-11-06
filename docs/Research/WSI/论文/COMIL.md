## Collaborative Optimization for Whole Slide Image Classification

> data: CAMELYON16、TCGA-Lung、TCGA-BRCA、TCGA-ESCA
>
> Knowledge-Based Systems 2026 · [论文](https://doi.org/10.1016/j.knosys.2025.114936)

#### 引言

让实例融合、邻域对比学习和 Transformer 包预测协同优化，通过跨伪包信息交互同时增强实例表示与切片决策。

#### 方法

（1）实例融合：结合历史和当前伪包信息增强表示。

（2）邻域对比：把相关伪包拉近，抑制不可靠的局部变化。

（3）协同优化：与 Transformer 包预测器联合训练，双向改进表征与决策。

##### 模型结构图

[![COMIL 模型结构](assest/COMIL/figure-2-complete.webp)](assest/COMIL/figure-2-complete.webp)

图 2（PDF 第 10 页）

#### 实验

##### 实验设置

四个分类基准，比较伪包和包级 MIL，并开展协同表示/预测消融。

##### 关键指标 { #key-results }

| 数据集 | ACC | AUC | F1 |
| --- | --- | --- | --- |
| TCGA-BRCA | 0.872 ± 0.031 | 0.907 ± 0.020 | 0.922 ± 0.019 |
| TCGA-ESCA | 0.905 ± 0.043 | 0.941 ± 0.031 | 0.923 ± 0.034 |

数据来源为原文表 2，PDF 第 19 页，ImageNet 预训练 ResNet18。

##### 结果解读

论文同时对照切片包与伪包方法。在 TCGA-ESCA 上，作者报告 ACC 比 DTFD 高 3.3 个百分点，比 ACMIL 高 2.0 个百分点。

##### 消融与讨论

检查跨伪包融合、邻域对比学习和 Transformer 聚合，关注协同训练是否优于单向优化。

#### 参考文献

> Collaborative Optimization for Whole Slide Image Classification
>
> Knowledge-Based Systems 2026 · [论文](https://doi.org/10.1016/j.knosys.2025.114936)
