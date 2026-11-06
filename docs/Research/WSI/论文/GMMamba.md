## GMMamba: Group Masking Mamba for Whole Slide Image Classification

> data: TCGA-BRCA、TCGA-ESCA、BRACS、TCGA-Lung
>
> ICCV 2025 · [论文](https://openaccess.thecvf.com/content/ICCV2025/html/Zheng_GMMamba_Group_Masking_Mamba_for_Whole_Slide_Image_Classification_ICCV_2025_paper.html)

#### 引言

在组内 Mamba 中学习稀疏掩码去除冗余，再以跨组超特征采样整合分散病灶，增强切片全局表征。

#### 方法

（1）位置分组：把切片划成较紧凑的局部实例组。

（2）IMM：在双向 Mamba 过程中学习掩码，去除组内低贡献模式。

（3）CSS：跨组采样判别特征，连接分散病灶与全局表示。

##### 模型结构图

[![GMMamba 模型结构](assest/GMMamba/figure-3-complete.webp)](assest/GMMamba/figure-3-complete.webp)

图 3（PDF 第 3 页）

#### 实验

##### 实验设置

按患者划分并做五折评估，报告 ACC/AUC/F1；还把 CSS 接入不同 MIL。

##### 关键指标 { #key-results }

| 数据集 | ACC | AUC | F1 |
| --- | --- | --- | --- |
| TCGA-BRCA | 0.891 ± 0.013 | 0.906 ± 0.016 | 0.932 ± 0.008 |
| TCGA-ESCA | 0.949 ± 0.029 | 0.970 ± 0.033 | 0.955 ± 0.025 |

数据来源为原文表 1，PDF 第 6 页，ImageNet 预训练 ResNet18。

##### 结果解读

同一特征配置下，GMMamba 相对 ACMIL 的 ACC 增益在 TCGA-ESCA 比 TCGA-BRCA 更大。论文另外把 CSS 模块接到其他 MIL 基线，检验采样策略能否单独带来收益。

##### 消融与讨论

考察分组策略、IMM 掩码比例和 CSS 变体，检查冗余去除与跨组信息汇总的互补。

#### 参考文献

> GMMamba: Group Masking Mamba for Whole Slide Image Classification
>
> ICCV 2025 · [论文](https://openaccess.thecvf.com/content/ICCV2025/html/Zheng_GMMamba_Group_Masking_Mamba_for_Whole_Slide_Image_Classification_ICCV_2025_paper.html)
