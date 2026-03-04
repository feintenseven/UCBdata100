# Lecture 8-Visualization II

Summary: Scatter Plot, Transformation, Visualization Theory

# Scatter Plot

数据点重合：缩小点的尺寸，调整透明度，jittering（加一点误差）

seaborn有更多功能，如linear model，jointmodel

**Hex Plot**

更粗略，平铺蜂窝图，数据多的地方颜色更深

**contour plot**

等高线图，数据更多-颜色更深-更高

## Transformation

把原始数据通过变换变成线性的

把skew的数据“挤”（squish）回来：用log

## Visualization Theory

### Information Channels

一个column-一个channel，类似于dimension，例如rgb图像就有3个channel

![image.png](Lecture%208-Visualization%20II/image.png)

### Harnessing Colour

注意使用色盲也可以辨认的颜色

### Harnessing Marks