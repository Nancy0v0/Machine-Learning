# Machine-Learning
## Week 1
碎碎念：一边学英文一边学ML
### Supervised Learning 监督学习

#### Regression 回归
监督学习的一种，通过学习x与y之间的映射关系，使只有x输入的情况下，利用监督学习得到y

#### Classification 分类

benign 良性 malignant 恶性（肿瘤）

类class和类别category是一个意思

分类就是预测应该属于哪个类别or离散类别

单个or多个输入都是可以的
![Z{N1W_``E7VLTND36X0D )S](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/4daeac49-566b-4d80-9033-e532539c7ea4)

### Unsupervised Learning 无监督学习
数据集没有标签

#### Clustering 聚类

Group similar data points together.

将未标记的数据放入不同的集群中

搜索，将包含某个关键词的聚类在一起

DNA，将不同的人的关于相同特征的DNA进行对比

定义：

Data only comes with input x,but not output labels y.Algorithm has to find structure in the data.

#### Anomaly detection 异常检测

检测异常事件

#### Dimensionality reducation 降维

将大数据集压缩成一个更小的数据集，同时丢失尽可能少的信息

### Liner Regression 线性回归模型

dataset 数据集

training set 训练集 训练模型的数据集

(x<sup>(1)</sup>,y<sup>(1)</sup>)，1指的是训练示例的编号

训练集包括输入特质和输出目标

![P_(WM`_5~~TYXT `QD7B}9C](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/f55f5d79-34a6-4cef-a5ee-58ebc5fd90c8)

f<sub>w,b</sub>(x)=wx+b

就是最小二乘法

