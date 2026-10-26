## Feature Re-Embedding: Towards Foundation Model-Level Performance in Computational Pathology

> data:
>
> **CAMELYON-16 [[1\]](javascript:void())** (C16)、**TCGA-BRCA**和**TCGA-NSCLC**
>
> **TCGA-LUAD、TCGA-LUSC 和 TCGA-BLCA**
>
> code: [Github](https://github.com/DearCaat/RRT-MIL)

#### 方法

$\begin{equation*} \hat{Y}\succ \mathcal{M}(X):=\mathcal{C}(\mathcal{A}(\mathcal{R}(\mathcal{F}(X)))), \tag{2} \end{equation*}$

创新点就是R()重新嵌入的映射函数

![image-20250527140327459](./assest/RRT-MIL/image-20250527140327459.png)

$\begin{align*} & \boldsymbol{ Step 1: } H \in \mathbb{R}^{I \times D} \xrightarrow{\text{Squaring }} H \in \mathbb{R}^{L^2 \times M^2 \times D}, \\ & \boldsymbol{ Step 2: } H \xrightarrow{\text{Partition }}\left\{H^l\right\}_{l=1}^{L^2}, H^l \in \mathbb{R}^{M \times M \times D},\\ & \boldsymbol{ Step 3: } \hat{Z}:=\left\{\hat{Z}^l\right\}_{l=1}^{L^2}, \hat{Z}^l=\mathcal{S}\left(H^l\right) \in \mathbb{R}^{M \times M \times D}, \tag{5} \end{align*}$

s()是EPEG

![image-20250527140455792](./assest/RRT-MIL/image-20250527140455792.png)

#### 结果

![image-20250527140628347](./assest/RRT-MIL/image-20250527140628347.png)

> 参考文献
>
> Tang, Wenhao et al. “Feature Re-Embedding: Towards Foundation Model-Level Performance in Computational Pathology.” *2024 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (2024): 11343-11352.
<!-- wsi-archive-enrichment -->

#### 论文信息与实验补充

> data: CAMELYON16、TCGA-BRCA、TCGA-NSCLC；TCGA-LUAD/LUSC/BLCA 生存任务
>
> CVPR 2024 · [论文](https://arxiv.org/abs/2402.17228) · [作者代码](https://github.com/DearCaat/RRT-MIL)

##### 方法补充

（1）区域内重嵌入：将离线特征重新组织成区域，提炼局部关系。

（2）位置增强：通过 EPEG 等位置编码补充组织空间线索。

（3）区域间联系：再次聚合区域信息，并将更新特征交给既有 MIL 预测器。

##### 实验设置

分类用 ACC/AUC/F1，预后用 C-index；C16 使用三次三折，其余数据主要采用五折评估。

##### 主要结果补充

核心证据是在线重嵌入同时增强 ResNet50 和 PLIP 特征，而非仅更换预训练编码器；不同特征与聚合器组合见主表。

##### 消融与讨论

比较区域关系、位置编码和重嵌入模块，并报告训练开销；预训练成本未包含在部分时间比较中。
