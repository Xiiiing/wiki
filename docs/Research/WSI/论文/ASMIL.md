## ASMIL: Attention-Stabilized Multiple Instance Learning for Whole Slide Imaging

> data: CAMELYON16、CAMELYON17、BRACS；附录生存与非 WSI 任务
>
> ICLR 2026 · [论文](https://openreview.net/forum?id=CYmjrbQRyM) · [作者代码](https://github.com/Linfeng-Ye/ASMIL)

#### 引言

以锚点模型稳定跨训练轮次的注意力，结合归一化 sigmoid 和随机 token 丢弃，同时缓解注意力震荡、过度集中及过拟合。

#### 方法

（1）锚点模型：提供相对稳定的注意力参考。

（2）归一化 sigmoid：缓解 softmax 使注意力集中于少数实例。

（3）随机 token 丢弃：减少过拟合，与锚点稳定共同训练。

<!-- wsi-complete-model -->
##### 模型结构图

**图 2 · 模型结构**（PDF 第 5 页）

[![ASMIL：图 2，模型结构](assest/ASMIL/figure-2-complete.webp)](assest/ASMIL/figure-2-complete.webp)

> 原文图注：Figure 2: Overview of ASMIL. Each WSI is divided into tiles and embedded into vision tokens using a pretrained encoder. These tokens, along with trainable FEAT tokens, feed into both online and anchor encoders. The anchor encoder’s atten- tion scores over the FEAT tokens are transformed into a prob- ability vector using an NSF, while the online encoder applies a softmax. To stabilize training and prevent the online model’s attention from becoming overly concentrated, we compute the KL divergence between the two distributions. Gradients are blocked to the anchor encoder using a stop-gradient (sg) oper- ator, and its parameters are updated via EMA from the online encoder. During training, we randomly drop (rd) N FEAT to- kens, feed the remaining tokens into a second transformer with a trainable [CLS] token, and train a classifier on its output.

[查看原尺寸](assest/ASMIL/figure-2-complete.webp)

<!-- /wsi-complete-model -->

#### 实验

##### 实验设置

主文比较 11 类注意力 MIL，以 F1/AUC 为主；数据处理、划分及训练设置位于附录 B。

##### 主要结果

完整 ASMIL 的增益与仅把锚点/归一化 sigmoid 插入其他模型的增益分开报告。

<!-- wsi-complete-results -->
##### 完整实验指标与对照

下列实验原页保留表头、全部行列、子图、误差说明和脚注，点击可查看原尺寸。比较时请对应相同的数据集、特征编码器和训练设置；`±`、置信区间、百分比和小数均保留原文的单位与统计口径。

| 原表/图中指标 | 读取方式 |
| --- | --- |
| ROC-AUC / AUROC | 越高越好；若原表明确为 PR-AUC，则按 PR 曲线面积读取 |
| F1 | 越高越好；保留 macro / weighted / micro 等平均方式 |
| C-index | 越高越好；用于生存预测，需保留终点及删失设置 |
| 时间 / FLOPs / 参数量 | 结合硬件、包长度和计时范围比较；小模型不一定推理更快 |

| 原文页 | 阅读内容 | 图表及正文引用 |
| --- | --- | --- |
| PDF 第 8 页 | 实验结果 | Table 1 |
| PDF 第 9 页 | 消融与参数分析 | Table 2、Table 3 |
| PDF 第 10 页 | 消融与参数分析 | Figure 4 |
| PDF 第 21 页 | 消融与参数分析 | Figure 7 |
| PDF 第 22 页 | 实验结果 | Table 4、Table 5 |
| PDF 第 23 页 | 实验结果 | Table 6、Table 7 |
| PDF 第 24 页 | 实验结果 | Table 8 |
| PDF 第 25 页 | 消融与参数分析 | Table 9、Figure 9 |
| PDF 第 26 页 | 消融与参数分析 | Figure 10、Table 10、Table 11 |
| PDF 第 27 页 | 实验结果 | Figure 11、Figure 12 |
| PDF 第 28 页 | 实验结果 | Table 12 |
| PDF 第 29 页 | 实验结果 | Table 13 |
| PDF 第 30 页 | 效率与开销 | Table 14、Table 15 |
| PDF 第 31 页 | 实验结果 | Table 16、Table 17 |
| PDF 第 32 页 | 实验结果 | Table 18 |
| PDF 第 39 页 | 实验结果 | Table 19 |

**实验原页 · PDF 第 8 页**（图表及正文引用：Table 1）

[![ASMIL：PDF 第 8 页完整实验内容](assest/ASMIL/experiment-page-08.webp)](assest/ASMIL/experiment-page-08.webp)

[查看原尺寸](assest/ASMIL/experiment-page-08.webp)

**实验原页 · PDF 第 22 页**（图表及正文引用：Table 4、Table 5）

[![ASMIL：PDF 第 22 页完整实验内容](assest/ASMIL/experiment-page-22.webp)](assest/ASMIL/experiment-page-22.webp)

[查看原尺寸](assest/ASMIL/experiment-page-22.webp)

**实验原页 · PDF 第 23 页**（图表及正文引用：Table 6、Table 7）

[![ASMIL：PDF 第 23 页完整实验内容](assest/ASMIL/experiment-page-23.webp)](assest/ASMIL/experiment-page-23.webp)

[查看原尺寸](assest/ASMIL/experiment-page-23.webp)

**实验原页 · PDF 第 24 页**（图表及正文引用：Table 8）

[![ASMIL：PDF 第 24 页完整实验内容](assest/ASMIL/experiment-page-24.webp)](assest/ASMIL/experiment-page-24.webp)

[查看原尺寸](assest/ASMIL/experiment-page-24.webp)

**实验原页 · PDF 第 27 页**（图表及正文引用：Figure 11、Figure 12）

[![ASMIL：PDF 第 27 页完整实验内容](assest/ASMIL/experiment-page-27.webp)](assest/ASMIL/experiment-page-27.webp)

[查看原尺寸](assest/ASMIL/experiment-page-27.webp)

**实验原页 · PDF 第 28 页**（图表及正文引用：Table 12）

[![ASMIL：PDF 第 28 页完整实验内容](assest/ASMIL/experiment-page-28.webp)](assest/ASMIL/experiment-page-28.webp)

[查看原尺寸](assest/ASMIL/experiment-page-28.webp)

**实验原页 · PDF 第 29 页**（图表及正文引用：Table 13）

[![ASMIL：PDF 第 29 页完整实验内容](assest/ASMIL/experiment-page-29.webp)](assest/ASMIL/experiment-page-29.webp)

[查看原尺寸](assest/ASMIL/experiment-page-29.webp)

**实验原页 · PDF 第 31 页**（图表及正文引用：Table 16、Table 17）

[![ASMIL：PDF 第 31 页完整实验内容](assest/ASMIL/experiment-page-31.webp)](assest/ASMIL/experiment-page-31.webp)

[查看原尺寸](assest/ASMIL/experiment-page-31.webp)

**实验原页 · PDF 第 32 页**（图表及正文引用：Table 18）

[![ASMIL：PDF 第 32 页完整实验内容](assest/ASMIL/experiment-page-32.webp)](assest/ASMIL/experiment-page-32.webp)

[查看原尺寸](assest/ASMIL/experiment-page-32.webp)

**实验原页 · PDF 第 39 页**（图表及正文引用：Table 19）

[![ASMIL：PDF 第 39 页完整实验内容](assest/ASMIL/experiment-page-39.webp)](assest/ASMIL/experiment-page-39.webp)

[查看原尺寸](assest/ASMIL/experiment-page-39.webp)

<details markdown="1">
<summary>展开消融、参数、数据设置及效率原页</summary>

**实验原页 · PDF 第 9 页**（图表及正文引用：Table 2、Table 3）

[![ASMIL：PDF 第 9 页完整实验内容](assest/ASMIL/experiment-page-09.webp)](assest/ASMIL/experiment-page-09.webp)

[查看原尺寸](assest/ASMIL/experiment-page-09.webp)

**实验原页 · PDF 第 10 页**（图表及正文引用：Figure 4）

[![ASMIL：PDF 第 10 页完整实验内容](assest/ASMIL/experiment-page-10.webp)](assest/ASMIL/experiment-page-10.webp)

[查看原尺寸](assest/ASMIL/experiment-page-10.webp)

**实验原页 · PDF 第 21 页**（图表及正文引用：Figure 7）

[![ASMIL：PDF 第 21 页完整实验内容](assest/ASMIL/experiment-page-21.webp)](assest/ASMIL/experiment-page-21.webp)

[查看原尺寸](assest/ASMIL/experiment-page-21.webp)

**实验原页 · PDF 第 25 页**（图表及正文引用：Table 9、Figure 9）

[![ASMIL：PDF 第 25 页完整实验内容](assest/ASMIL/experiment-page-25.webp)](assest/ASMIL/experiment-page-25.webp)

[查看原尺寸](assest/ASMIL/experiment-page-25.webp)

**实验原页 · PDF 第 26 页**（图表及正文引用：Figure 10、Table 10、Table 11）

[![ASMIL：PDF 第 26 页完整实验内容](assest/ASMIL/experiment-page-26.webp)](assest/ASMIL/experiment-page-26.webp)

[查看原尺寸](assest/ASMIL/experiment-page-26.webp)

**实验原页 · PDF 第 30 页**（图表及正文引用：Table 14、Table 15）

[![ASMIL：PDF 第 30 页完整实验内容](assest/ASMIL/experiment-page-30.webp)](assest/ASMIL/experiment-page-30.webp)

[查看原尺寸](assest/ASMIL/experiment-page-30.webp)

</details>

<!-- /wsi-complete-results -->

##### 消融与讨论

分别考察锚点稳定、归一化 sigmoid 和 token 丢弃，检查跨 epoch 注意力波动而非只看最终热图。

#### 参考文献

> ASMIL: Attention-Stabilized Multiple Instance Learning for Whole Slide Imaging
>
> ICLR 2026 · [论文](https://openreview.net/forum?id=CYmjrbQRyM) · [作者代码](https://github.com/Linfeng-Ye/ASMIL)
