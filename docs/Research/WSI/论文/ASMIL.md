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

#### 实验

##### 实验设置

主文比较 11 类注意力 MIL，以 F1/AUC 为主；数据处理、划分及训练设置位于附录 B。

##### 主要结果

完整 ASMIL 的增益与仅把锚点/归一化 sigmoid 插入其他模型的增益分开报告。

##### 消融与讨论

分别考察锚点稳定、归一化 sigmoid 和 token 丢弃，检查跨 epoch 注意力波动而非只看最终热图。

#### 参考文献

> ASMIL: Attention-Stabilized Multiple Instance Learning for Whole Slide Imaging
>
> ICLR 2026 · [论文](https://openreview.net/forum?id=CYmjrbQRyM) · [作者代码](https://github.com/Linfeng-Ye/ASMIL)
