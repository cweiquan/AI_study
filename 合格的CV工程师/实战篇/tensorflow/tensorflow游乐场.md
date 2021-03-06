# tensorflow游乐场

## tensorflow playground简介

TensorFlow游乐场是一个通过网页浏览器就可以训练简单神经网络 并实现了可视化训练过程的工具。

地址：http://playground.tensorflow.org/

## TensorFlow playground使用

### TensorFlow playground界面

![img](../image/tensorflowPlayground.png)

### TensorFlow playground界面示意图

![tensorflowPlayground示意图](../image/tensorflowPlayground示意图.png)

### 功能详解

#### （1）控制运行

从左到右三个功能分别是：（a）重启；（b）运行；（c）一次运行一个周期

#### （2）运行周期数

用于查看训练的周期数

#### （3）参数调整区域

| 名称           | 功能说明                                                     |
| :------------- | ------------------------------------------------------------ |
| Learning rate  | 学习率（是一个超参数，在梯度下降算法中会用到；学习率是人为根据实际情况来设定）。 |
| Activation     | 激活函数（默认为非线性函数Tanh；如果对于线性分类问题，这里可以不使用激活函数）。 |
| Regularization | 正则化（正则化是利用范数解决过拟合的问题）。                 |
| Problem type   | 问题类型（在这里我们要解决的是一个二分类问题，简单解释一下分类问题是指，给定一个新的模式，根据训练集推断它所对应的类别（如：+1，-1），是一种定性输出，也叫离散变量预测；回归问题是指，给定一个新的模式，根据训练集推断它所对应的输出值（实数）是多少，是一种定量输出，也叫连续变量预测；在这里我们属于分类问题。）。 |

#### （4）数据区域

| 名称                      | 说明                                                         |
| ------------------------- | ------------------------------------------------------------ |
| DATA                      | 数据集类型（这里提供了四种数据集，我们默认选中第一种；被选中的数据也会显示在最右侧的OUTPUT中；在这个数据中，我们可以看到二维平面上有蓝色和黄色的小点；每一个小点代表一个样例例子；点的颜色代表样例的标签；因为只有两种颜色，所以这里是一个二分类问题；在这里我们以判断某工厂零件是否合格为例子来说明，那么黄色就代表不合格零件，蓝色就代表合格零件）。 |
| Ratio of training to test | 数据用于测试的比例（直接对进度条进行操作即可调整）。         |
| Noise                     | 对数据中引入噪声。                                           |
| Batch size                | 调整batch size的大小。                                       |

#### （5）网络结构调整区域

| 名称          | 说明                                                         |
| ------------- | ------------------------------------------------------------ |
| FEATURES      | 特征向量（为了将一个实际问题对应到空间中的点，我们需要提取特征。在这里我们可以用零件的长度和质量来大致描述；所以这里x1就代表零件长度，x2代表零件质量;特征向量是神经网络的输入）。 |
| HIDDEN LAYERS | 隐藏层（在输入和输出之间的神经网络称为隐藏层；一般神经网络的隐藏层越多这个神经网络越深；这里我们默认有一个隐藏层，这个隐藏层上有4个节点）。 |

直接通过点击各个图标即可选择Features的类型，对于隐藏层的操作，可以直接选择加减号即可获得想要的隐藏层层数以及每层的神经元个数。

#### （6）输出结果区域

设置完上面的参数，点击运行即可观测到输出结果的变化。

如果你选择的是分类问题，即可看到明显的边界变化以及loss在不断减小的情况，点击show test data可以显示未参与训练的test数据集的情况，点击Discretize output可以看到离散化后的结果。

### 演示

参数设置：学习率0.03，激活函数Tanh，正则项L1 比例0.001，问题类型Classification

数据：选择左上第一个

网络结构：选择含两个隐藏层，第一个隐藏层4个神经元，第二个隐藏层2个神经元

![深度录屏_选择区域_20190530114647](../image/深度录屏_选择区域_20190530115657.gif)

参考自：https://www.jianshu.com/p/95d46de63408



![点关注不迷路，我们一起上高速](../image/默认标题_横版二维码_2019.05.30.jpg)

