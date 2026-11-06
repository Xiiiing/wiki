## AttriMIL: Revisiting attention-based multiple instance learning for whole-slide pathological image classification from a perspective of instance attributes

> data: CAMELYON16、CAMELYON17、BCNB、TCGA-NSCLC、UniToPatho
>
> Medical Image Analysis 2025 · [论文](https://doi.org/10.1016/j.media.2025.103631) · [作者代码](https://github.com/MedCAI/AttriMIL)

#### 引言

注意力权重表示聚合时给实例多少权重，实例对某个类别的贡献还由分类头决定。AttriMIL 用类别专属的属性分数刻画这个贡献，并约束切片内外的相关实例。

#### 方法

多分支评分联合注意力与分类头。区域约束利用切片内的空间邻近，切片约束利用不同切片的实例相似性。病理自适应编码器进一步用目标任务信号调整特征。

##### 模型结构图

[![AttriMIL 模型结构](assest/AttriMIL/figure-2-complete.webp)](assest/AttriMIL/figure-2-complete.webp)

图 2（PDF 第 4 页）

#### 实验

##### 实验设置

覆盖肿瘤检测、腋窝淋巴结转移预测、肺癌亚型、肿瘤分级及外部泛化。

##### 关键指标 { #key-results }

| 配置 | AUC | F1 | ACC |
| --- | --- | --- | --- |
| TransMIL | 0.701 ± 0.029 | 0.511 ± 0.077 | 0.655 ± 0.031 |
| TransMIL + AttriMIL | 0.735 ± 0.015 | 0.578 ± 0.038 | 0.698 ± 0.013 |

数据来源为原文表 2，PDF 第 8 页，BCNB，ImageNet 预训练 ResNet-18。

##### 结果解读

在 ImageNet 预训练 ResNet-18 的 BCNB 实验中，AttriMIL 提高了 TransMIL 的切片分类结果。论文另外用定位评价检查属性分数能否指出病灶。

##### 消融与讨论

分别考察多分支属性评分、区域约束、切片约束与病理自适应学习，区分切片分类和病灶定位证据。
