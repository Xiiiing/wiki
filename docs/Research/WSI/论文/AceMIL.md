## AceMIL: Ordinal-Aware Multiple Instance Learning for Pathological Progression Analysis

> data: NAS-8s、CAMELYON17 pN-stage、TUPAC16
>
> CVPR 2026（会议目录收录；方法简介依据收藏 PDF） · [会议目录](https://media.eventhosts.cc/Conferences/CVPR2026/CVPR_main_conf_2026_15.pdf) · 原文依据本地 PDF；作者代码地址本次访问返回 404

#### 引言

将病理进展建模为有序回归，以退火软标签保留分期顺序，并结合差分 Transformer 和 patch 级阶段聚合减少严重程度错序。

#### 方法

（1）有序目标：用退火软标签表达分期之间的顺序。

（2）差分编码：突出与阶段差异有关的组织特征。

（3）局部阶段聚合：使 patch 证据与整片有序预测相协调。

![AceMIL：方法相关图示](assest/AceMIL/method-archive.webp)

原文Figure 2，PDF 第 4 页。

#### 实验

##### 实验设置

五折评价有序病理分期，主要看加权 Kappa，同时保留分类指标。

##### 主要结果

摘要报告三个任务 Kappa 增益为 6.42、7.57、1.51 个百分点；需结合对应基线与方差读表。

##### 消融与讨论

比较退火软标签、差分 Transformer 和局部阶段聚合，检查是否减少跨级严重误判。

#### 参考文献

> AceMIL: Ordinal-Aware Multiple Instance Learning for Pathological Progression Analysis
>
> CVPR 2026（会议目录收录；方法简介依据收藏 PDF） · [会议目录](https://media.eventhosts.cc/Conferences/CVPR2026/CVPR_main_conf_2026_15.pdf) · 原文依据本地 PDF；作者代码地址本次访问返回 404
