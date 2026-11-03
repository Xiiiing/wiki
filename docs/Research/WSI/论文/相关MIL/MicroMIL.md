## MicroMIL: Graph-Based Multiple Instance Learning for Context-Aware Diagnosis with Microscopic Images

> data: Seegene 结肠癌显微镜数据、BreakHis
>
> MICCAI 2025（PDF 与作者代码；2024 预印本合并） · [论文](https://papers.miccai.org/miccai-2025/0566-Paper0707.html) · [作者代码](https://github.com/kimjongwoo-cell/MicroMIL)

#### 引言

面向普通光学显微镜采集图像，以聚类和 Gumbel-Softmax 选择代表图像，再按特征相似度建图，无需绝对空间坐标。

#### 方法

（1）RIE：以深度聚类和 hard Gumbel-Softmax 选取代表图像。

（2）相似度图：按余弦相似度连接代表节点，无需绝对坐标。

（3）图聚合：学习局部与跨图像上下文，生成患者级预测。

<!-- wsi-complete-model -->
##### 模型结构图

**图 2 · 模型结构**（PDF 第 4 页）

[![MicroMIL：图 2，模型结构](../assest/MicroMIL/figure-2-complete.webp)](../assest/MicroMIL/figure-2-complete.webp)

> 原文图注：Fig. 2. Proposed end-to-end MicroMIL framework.

[查看原尺寸](../assest/MicroMIL/figure-2-complete.webp)

<!-- /wsi-complete-model -->

#### 实验

##### 实验设置

按患者组织图像包，并模拟冗余图像比例变化；BreakHis 含 7,909 张图像、81 位患者。

##### 主要结果

高冗余训练/测试设置使部分基线退化，MicroMIL 在相关对照中更稳定；输入无需已知绝对空间位置。

<!-- wsi-complete-results -->
##### 完整实验指标与对照

下列实验原页保留表头、全部行列、子图、误差说明和脚注，点击可查看原尺寸。比较时请对应相同的数据集、特征编码器和训练设置；`±`、置信区间、百分比和小数均保留原文的单位与统计口径。

| 原文页 | 阅读内容 | 图表及正文引用 |
| --- | --- | --- |
| PDF 第 6 页 | 实验结果 | Table 1 |
| PDF 第 7 页 | 实验结果 | Figure 4 |
| PDF 第 8 页 | 实验结果 | Figure 5、Figure 6、Table 2 |

**实验原页 · PDF 第 6 页**（图表及正文引用：Table 1）

[![MicroMIL：PDF 第 6 页完整实验内容](../assest/MicroMIL/experiment-page-06.webp)](../assest/MicroMIL/experiment-page-06.webp)

[查看原尺寸](../assest/MicroMIL/experiment-page-06.webp)

**实验原页 · PDF 第 7 页**（图表及正文引用：Figure 4）

[![MicroMIL：PDF 第 7 页完整实验内容](../assest/MicroMIL/experiment-page-07.webp)](../assest/MicroMIL/experiment-page-07.webp)

[查看原尺寸](../assest/MicroMIL/experiment-page-07.webp)

**实验原页 · PDF 第 8 页**（图表及正文引用：Figure 5、Figure 6、Table 2）

[![MicroMIL：PDF 第 8 页完整实验内容](../assest/MicroMIL/experiment-page-08.webp)](../assest/MicroMIL/experiment-page-08.webp)

[查看原尺寸](../assest/MicroMIL/experiment-page-08.webp)

<!-- /wsi-complete-results -->

##### 消融与讨论

考察代表图像提取与相似度图聚合，并在冗余迁移实验中检验去重能力。

#### 参考文献

> MicroMIL: Graph-Based Multiple Instance Learning for Context-Aware Diagnosis with Microscopic Images
>
> MICCAI 2025（PDF 与作者代码；2024 预印本合并） · [论文](https://papers.miccai.org/miccai-2025/0566-Paper0707.html) · [作者代码](https://github.com/kimjongwoo-cell/MicroMIL)

本文归入相关 MIL 方法：具体研究对象见数据与实验设置。
