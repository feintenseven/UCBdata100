# Lecture 14-Gradient Decent

## sklearn

1 Initialize a new model

`my_model=lm.LinearRegression()`

参数fit_intercept决定是否添加一列bias(1)

2 Fit the model to the training data

`my_model.fit(x,y)`

3 Use fitted model to make prediction

`my_model.predict(x_new)`

## Gradient Decent

沿斜率下降，找到最小值

## Gradient Descent 更新公式

$x^{(t+1)} = x^{(t)} - \alpha f'(x^{(t)})$

### 含义

- $x^{(t)}$：第 t 次迭代时的参数
- $x^{(t+1)}$：下一次更新后的参数
- $f'(x^{(t)})$：函数在当前点的导数（梯度）
- $\alpha$：学习率（step size），可随着次数decay