# Lecture 6-Regular Expressions

Summary: Panda str Methods, RegEx

## Panda str Methods

Series.str.<str operations>

![image.png](Lecture%206-Regular%20Expressions/image.png)

## Regular Expressions

正则表达式

![图片3.png](Lecture%206-Regular%20Expressions/%E5%9B%BE%E7%89%873.png)

![图片4.png](Lecture%206-Regular%20Expressions/%E5%9B%BE%E7%89%874.png)

![图片1.png](Lecture%206-Regular%20Expressions/%E5%9B%BE%E7%89%871.png)

![图片2.png](Lecture%206-Regular%20Expressions/%E5%9B%BE%E7%89%872.png)

![图片5.png](Lecture%206-Regular%20Expressions/%E5%9B%BE%E7%89%875.png)

() specifies a capture group 只会返回用（）括起来的部分（tuple in list）

`series.str.findall()`

`se.str.extract(pattern)` Return a df of each capture group’s first match in the string

`se.str.extractall()`

`re.sub(pattern,repl,text)` 把和pattern匹配的东西全部变成repl

`series.str.replace(pattern,repl,regex=True)`