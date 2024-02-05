# Week 2
## Multiple features 多维特征

![DMR}8~U_E)R0$7UF J@U}I](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/b16104e8-a5e8-41e8-b7aa-d6db771809ce)

线代部分

多元线性回归

## Vectorization 向量化

调包：Numpy

$`f_{\overrightarrow{\mathrm{w}}, b}(\overrightarrow{\mathrm{x}})=\overrightarrow{\mathrm{w}} \cdot \overrightarrow{\mathrm{x}}+b`$

其用代码表示为：

```
import Numpy
f = np.dot(w,x)+b
```
将w，x进行向量化点乘

比用for循环的效率高

![D$HNUU%`Z@_4LLWT61G 4W7](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/29fd77b3-979b-4da2-8a71-202ef87b696d)

并不算空间换时间，而是硬件并行计算出来的

## Gradient Descent for Multiple Regression 多元线性回归的梯度下降

![image](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/513b91f1-3100-40fd-98c9-1a206a624da3)

![V(5)YD% SYJVB@E_9Z 2TY3](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/5c0c8176-38e8-435f-9708-9d0febaf3ab7)

把之前的公式的w，x换成向量形式

Normal equation：使用高级线性代数库进行计算，不用梯度下降。如果特征数量很大，正规方程也算的很慢。基本上是不用的。

## Feature Scaling 特征缩放

当一个特征值的可能范围很大的时候，一个好的模型更可能会选择一个相对较小的参数值；同理，当特征的可能值很小时，其参数的合理值将相对较大。
![({3TY(S~VR 4UI W1UA_18](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/ac7f5b4e-4c9b-403b-ac9b-b6fe078fb3f1)

从上图可以看出，x1的变化范围很大，所以w1改变一点点，对其代价函数的变化就很大

![~I%HF KACJ$EE%@6(RR9DCI](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/cb3df225-71b7-4aa7-b6ce-8a5914fc2d58)

这个图就是x2的变化范围小一些，J的等高线图更像一个圆圈，这样的梯度下降可以更快找到一条通往全局最小值的路径

方法1：**Feature Scaling缩放**

除以该特征范围的最大值，实现归一化

![A{ F@ 24BI K9UNCWJ`M_NX](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/2c2de3ae-51b8-49ee-bcee-56910349f838)

**Mean normalization 均值归一化**

首先，获得均值μ（所有值的均值，而不是只有上下的均值）。然后取每个x1与μ相减，除以范围

![}V_CA9F6L8I9Z Z0}J3 ZJ](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/2499e36f-91ee-42b6-94d9-075854a713da)

**Z-score normalization**

计算σ标准差。然后取每个x1与μ相减，除以标准差

![O1C{58SWDE8C`D4FX3P(LF6](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/ee017f02-f97b-41e7-abf9-f1d4dbe4ca9d)

但缩放区间也不一定是[-1,1]，都是ok的
