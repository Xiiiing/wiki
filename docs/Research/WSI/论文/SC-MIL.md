## SC-MIL: Supervised Contrastive Multiple Instance Learning for Imbalanced Classification in Pathology

> data: TCGA-NSCLC、TCGA-RCC，及域外来源的同类亚型数据
>
> WACV 2024 · [论文](https://openaccess.thecvf.com/content/WACV2024/html/Juyal_SC-MIL_Supervised_Contrastive_Multiple_Instance_Learning_for_Imbalanced_Classification_in_WACV_2024_paper.html)

#### 引言

将监督式对比学习应用于包表示，并逐步从表征学习转向分类器学习，处理数据集类别不平衡及阳性切片中病灶稀少的问题。

#### 方法

（1）包级对比：在切片嵌入之间应用监督对比损失，避免给所有 patch 赋同一标签。

（2）分类学习：以交叉熵学习最终决策边界。

（3）平滑过渡：训练中逐步调整两类目标的侧重，处理标签不平衡。

##### 模型结构图

[![SC-MIL 模型结构](assest/SC-MIL/figure-2-complete.webp)](assest/SC-MIL/figure-2-complete.webp)

图 2（PDF 第 3 页）

#### 实验

##### 实验设置

按病例隔离划分 60:15:25；只调整训练集不平衡比例，固定验证/测试集。

##### 关键指标 { #key-results }

| 测试集 | F1（%） | AUC（%） |
| --- | --- | --- |
| TCGA-NSCLC | 84.05 ± 2.65 | 91.64 ± 1.81 |
| OOD-NSCLC | 41.5 ± 8.23 | 92.97 ± 1.95 |

数据来源为原文表 5–6，PDF 第 5 页，SC-MIL-RS，训练不平衡比 10。

##### 结果解读

在训练不平衡比 10 下，域外 AUC 仍超过 0.92，F1 却跌至 41.5%。模型仍能对样本排序，但固定决策阈值下的分类表现受域偏移影响较大。

##### 消融与讨论

比较对比损失与交叉熵的联合/顺序训练，并考察训练权重调度；必须防止患者跨划分泄漏。

#### 参考文献

> SC-MIL: Supervised Contrastive Multiple Instance Learning for Imbalanced Classification in Pathology
>
> WACV 2024 · [论文](https://openaccess.thecvf.com/content/WACV2024/html/Juyal_SC-MIL_Supervised_Contrastive_Multiple_Instance_Learning_for_Imbalanced_Classification_in_WACV_2024_paper.html)
