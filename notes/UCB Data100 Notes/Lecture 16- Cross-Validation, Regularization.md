# Lecture 16- Cross-Validation, Regularization

## Polynomial Features

用多维去拟合数据，避免数据关系非线性

degree=n，用n次式来拟合

问题：可能出现过拟合

## Validation Set

![image.png](Lecture%2016-%20Cross-Validation,%20Regularization/image.png)

reuse validation set

### K-Fold Cross-Validation

分成k份，分别取k份作为validation set，得到k个误差，算误差均值，得到该degree下的预期泛化能力

### Hyper Parameter

超参数，由人工选择的参数（例如degree）

## Regularization

constrain the parameters 限制参数大小，参数绝对值越小，对应的degree的影响越小

### L1 Regularization(LASSO)

解决问题：对噪声的拟合（小theta）

适合做**特征选择（找到更重要的那一项）**

在OLS后面加上一个惩罚项α*sum(θ)，α是超参数。

当α很大时，很多小theta都会变成0。

当α较小时，部分小theta会被压缩。

![image.png](Lecture%2016-%20Cross-Validation,%20Regularization/image%201.png)

### L2 Regularization(Ridge)

结局问题：LASSO面对多重线性可能会随机选取一个theta来缩小

类似LASSO，改变惩罚项为λsum(θ^2)

更适合**多重共线性**

![image.png](Lecture%2016-%20Cross-Validation,%20Regularization/image%202.png)