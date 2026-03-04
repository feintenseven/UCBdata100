# Lecture 7-Visualization I

Summary: Bar Plot, Histogram, Box Plot, Violin Plot, KDE Curve

Bar plot：qualitative

Histogram（频率直方图）：quantitative

# Bar Plot

## Matplotlib

`plt.example_plotting_funxtion(x_values,y_values)`

`plt.xlabel(”x axis label”)`

`plt.ylabel(”y axis label”)`

`plt.title(”title of the plot”)`

`plt.bar(x,y)`

![image.png](Lecture%207-Visualization%20I/image.png)

## Seaborn

`sns.countplot(data=dataframename, x=’column’)` 生成柱状图，自动计算y轴（x轴元素的出现次数）

# Histogram

![image.png](Lecture%207-Visualization%20I/image%201.png)

skew:

positive: mean > median 前高后低

negative: mean < median 前低后高

![image.png](Lecture%207-Visualization%20I/image%202.png)

![image.png](Lecture%207-Visualization%20I/image%203.png)

# Box Plot

![image.png](Lecture%207-Visualization%20I/image%204.png)

# Violin Plot

外层：核密度图（kde curve）

内部：箱图

# KDE Curve

**Kernel Density Estimation**

Step 1: Place a kernel at each point (usually alpha=1)

Step 2: Normalize kernels so that total area is 1

Step 3: Sum all kernels together

sns有内置函数，可以直接画出kde curve