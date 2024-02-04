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

x：输入 输入特征
f：模型
y：模型的输出 预测

### Cost Function 代价函数
误差
$`J(w,b)=\frac{1}{2m} \sum_{i=1}^m\left(\begin{array}{c}\hat{y}^{(i)}-y^{(i)}\end{array}\right)^2`$

$`J(w, b)=\frac{1}{2 m} \sum_{i=1}^m\left(f_{w, b}\left(x^{(i)}\right)-y^{(i)}\right)^2`$

使J尽可能地小，找到使J最小的w和b

### 可视化代价函数

![image](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/25298e81-4ffe-4426-9452-2c4f3f2cadc1)

最后可以得到一个类似等高线的东西
![E4YE%LAU WK}C4{79V@{%{G](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/9dd1f864-a976-454d-8ad0-407c5faca03f)

### 可视化举例

![XJ1JHP 54W U_O6FN(~$$21](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/6db7aa3b-32f6-4955-ae3f-ce03c4ad85b9)
左图的竖线差表示的是y预测和y实际之间的差值，右图的点距离中心点（成本点，就是圆圈最密集的地方）的差距是代价

梯度下降帮助我们自动寻找到最小的w和b

### Gradient Descent 梯度下降

梯度下降可以用于尝试最小化任何函数的算法，不仅仅是线性回归的成本函数

不停更改w，b的值，使J极小

可能存在不止一个极小值

这不是数学公式，是代码，右边赋值给左边

$`w=w-\alpha \frac{\partial}{\partial w} J(w, b)`$

$`b=b-\alpha \frac{\partial}{\partial w} J(w, b)`$

α学习率
code：
![VNN AW$RAT93 ~XTH%AE`CE](https://github.com/Nancy0v0/Machine-Learning/assets/84230854/2357a3c6-d668-416c-a9d1-ec650734f89a)
