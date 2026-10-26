## Fast and Accurate Gigapixel Pathological Image Classification with Hierarchical Distillation Multi-Instance Learning

> data:
>
> **CAMELYON16**
>
>  **TCGA-NSCLC**
>
>  **TCGA-BRCA**
>
> code: [Github]( https://github.com/JiuyangDong/HDMIL)

#### 方法

![image-20250608162423506](./assest/HDMIL/image-20250608162423506.png)

#### 结果

![image-20250608163102469](./assest/HDMIL/image-20250608163102469.png)

> 参考文献
>
> Dong, Jiuyang et al. “Fast and Accurate Gigapixel Pathological Image Classification with Hierarchical Distillation Multi-Instance Learning.” *ArXiv* abs/2502.21130 (2025): n. pag.
<!-- wsi-archive-enrichment -->

#### 论文信息与实验补充

> data: CAMELYON16、TCGA-NSCLC、TCGA-BRCA
>
> CVPR 2025 · [论文](https://arxiv.org/abs/2502.21130) · [作者代码](https://github.com/JiuyangDong/HDMIL)

##### 方法补充

（1）DMIN：高倍率动态 MIL 产生分类与相关区域信号。

（2）LIPN：学习低倍率区域是否值得进行高倍率编码，提前过滤无关 patch。

（3）CKA：用 Chebyshev 多项式构建可学习分类函数，增强最终决策。

##### 实验设置

十次 Monte Carlo 评估；C16 保留官方测试集，TCGA 按病例 8:1:1 划分，另拆分四个推理阶段计时。

##### 主要结果补充

HDMIL† 只运行 DMIN，HDMIL 先用 LIPN；C16 中预筛会略降 AUC，TCGA 上两者差距更小。

##### 消融与讨论

比较 DMIN、低倍率预筛和 CKA 分类器；速度应包含预筛、裁块、编码与聚合，而非只算分类头。
