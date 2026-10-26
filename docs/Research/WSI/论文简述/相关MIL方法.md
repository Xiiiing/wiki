# 相关 MIL 方法

以下论文同样来自 2024–2026 年收藏，涵盖显微镜图像、其他医学影像和通用多实例学习。每条注明研究对象，便于与 WSI 方法区分和交叉参考。

[返回论文简述索引](index.md)

## LaDM³IL

**A Label Disambiguation-Based Multimodal Massive Multiple Instance Learning Approach for Immune Repertoire Classification**

AAAI 2024（PDF 出版信息） · [作者代码](https://github.com/Josie-xufan/LaDM3IL)

面向免疫组库分类，将基因片段和氨基酸序列进行多模态融合，并用标签消歧缓解海量实例中的监督噪声。属于跨领域 MIL 方法。

## PE-MIL

**Prompt-Enhanced Multiple Instance Learning for Weakly Supervised Video Anomaly Detection**

CVPR 2024 · [论文](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_Prompt-Enhanced_Multiple_Instance_Learning_for_Weakly_Supervised_Video_Anomaly_Detection_CVPR_2024_paper.html) · [作者代码](https://github.com/Junxi-Chen/PE-MIL)

利用异常感知提示与正常上下文提示增强视频片段特征，改善弱监督视频异常检测的事件识别与边界定位。研究对象为视频。

## HybridMIL

**Hybrid multiple instance learning network for weakly supervised medical image classification and localization**

Expert Systems with Applications 2025 · [论文](https://doi.org/10.1016/j.eswa.2024.125362)

将 CNN 与宽度学习系统结合，通过实例特征增强、全局语义增强和混合特征融合完成弱监督分类与定位，属于通用医学图像 MIL。

收藏在 2024 年目录，按出版卷期归入 2025 年。

## DKMIL

**Data-Driven Knowledge Fusion for Deep Multi-Instance Learning**

IEEE Transactions on Neural Networks and Learning Systems 2025 · [论文](https://doi.org/10.1109/TNNLS.2024.3436944)

从关键样本的决策中提取数据驱动知识，再用知识融合和两级注意力支持深度 MIL，重点是通用 MIL 的知识复用。

收藏在 2024 年目录，按出版卷期归入 2025 年。

## RGMIL

**Reinforced GNNs for Multiple Instance Learning**

IEEE Transactions on Neural Networks and Learning Systems 2025 · [论文](https://doi.org/10.1109/TNNLS.2024.3392575) · [作者代码](https://github.com/RingBDStack/RGMIL)

使用多智能体强化学习同步调整包内图结构和图神经网络架构，学习两者的关联，减少图构建与网络选择分离带来的限制。

收藏在 2024 年目录，按出版卷期归入 2025 年。

## PSTR / RankMIL

**Partial Scene Text Retrieval**

IEEE TPAMI 2024（PDF 出版信息） · [论文](https://arxiv.org/abs/2411.10261) · [作者代码](https://github.com/lanfeng4659/PSTR)

将查询文本与场景文字映射到共享空间，用排序 MIL 过滤噪声，并以动态部分匹配检索文字行内部片段。研究对象为场景文字检索。

## WMRE

**WMRE: Enhancing Distant Supervised Relation Extraction with Word-level Multi-instance Learning and Multi-hierarchical Feature**

ICASSP 2025 · [论文](https://doi.org/10.1109/ICASSP49660.2025.10890115)

在词级别筛选注意力并提取多层次文本特征，降低远程监督关系抽取中的噪声。研究对象为自然语言关系抽取。

## PMITra

**Cross-domain pedestrian trajectory prediction via behavioral pattern-aware multi-instance GCN**

Knowledge-Based Systems 2025 · [论文](https://doi.org/10.1016/j.knosys.2025.114266)

通过行为模式聚类、多实例图卷积及模式对齐实现跨域行人轨迹预测，属于跨领域 MIL 方法。

## MSTNet

**MSTNet: Multi-scale spatial-aware transformer with multi-instance learning for diabetic retinopathy classification**

Medical Image Analysis 2025 · [论文](https://doi.org/10.1016/j.media.2025.103511)

结合双路多尺度 Transformer、空间感知模块和 MIL 聚合，建模眼底微小病灶及上下文，用于糖尿病视网膜病变分级。

## FPN-MIL

**Multi-scale Attention-Based Multiple Instance Learning for Breast Cancer Diagnosis**

MICCAI 2025 · [论文](https://doi.org/10.1007/978-3-032-05182-0_36) · [作者代码](https://github.com/marianamourao-37/Multi-scale-Attention-based-MIL)

在乳腺 X 线影像中结合特征金字塔、多尺度实例聚合和深层监督，兼顾肿块与钙化病灶的不同尺度。研究对象为乳腺摄影。

## MicroMIL

**MicroMIL: Graph-Based Multiple Instance Learning for Context-Aware Diagnosis with Microscopic Images**

MICCAI 2025（PDF 与作者代码；2024 预印本合并） · [论文](https://papers.miccai.org/miccai-2025/0566-Paper0707.html) · [作者代码](https://github.com/kimjongwoo-cell/MicroMIL)

面向普通光学显微镜采集图像，以聚类和 Gumbel-Softmax 选择代表图像，再按特征相似度建图，无需绝对空间坐标。

## MoMIL

**MoMIL: Mixture of Multi-Instance Learners for Modeling Multiple Compound Activities in High Content Imaging**

MICCAI 2025 · [论文](https://papers.miccai.org/miccai-2025/0578-Paper1746.html)

在高内涵细胞成像中，以共享编码器和实验任务专属 MIL 学习器预测化合物活性，缓解多任务标签稀疏问题。研究对象为药物筛选。

## 超声 MIL 校准研究

**Calibration in Multiple Instance Learning: Evaluating Aggregation Methods for Ultrasound-Based Diagnosis**

MICCAI 2025 · [论文](https://doi.org/10.1007/978-3-032-05182-0_6)

比较多种聚合器在域内和域外超声诊断中的概率校准，分析分类判别力与预测过度自信之间的权衡。文件名 UBD-MIL 不是正文方法名。

## GDF-MIL

**Rethinking Multi-Instance Learning Through Graph-Driven Fusion: A Dual-Path Approach to Adaptive Representation**

AAAI 2026 · [论文](https://doi.org/10.1609/aaai.v40i34.40081)

用软聚类压缩实例并学习动态稀疏图，再通过门控融合图特征与包级语义特征；属于跨任务的通用图 MIL 框架。

## GVL-MIL

**Generative Vision-Language Multiple Instance Learning for Weakly Supervised Neonatal Fundus Screening and Reporting**

收藏标记 CVPR 2026；本次核对 PDF，会议归属待核实 · [作者代码](https://github.com/CVIU-CSU/GVL-MIL)

微调生成式视觉语言模型以产生新生儿眼底实例描述，再通过双分支 MIL 和熵感知融合进行筛查。研究对象为新生儿眼底图像。

## LML / MPEM

**Learning from Majority Label: A Novel Problem in Multi-class Multiple-Instance Learning**

收藏标记 Pattern Recognition 2026；所附链接为 arXiv 2025 版本 · [论文](https://arxiv.org/abs/2509.04023) · [作者代码](https://github.com/Shiku-Kaito/Learning-from-Majority-Label-A-Novel-Problem-in-Multi-class-Multiple-Instance-Learning)

研究包标签等于实例多数类别的多类 MIL，以计数网络和多数比例增强模块学习实例分类；其标签假设与经典阳性包 MIL 不同。
