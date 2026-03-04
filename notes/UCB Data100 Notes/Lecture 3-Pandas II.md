# Lecture 3-Pandas II

Summary: Conditional Selection, Boolean Operator, Adding, Removing, and Modifying Columns, Utility Functions, Custom Sort

## Conditional  Selection

- 用boolean筛选

`df.iloc[]`和`df[]`都接受一个和df等长（index）的boolean list。保留true的删除false的

- 用logical operator生成boolean再筛选

`df[”column”]==”a”` 得到一个column下a为true的boolean series

然后可以直接`df[boolean series]`或者`df.loc[boolean series]`来筛选

### Boolean Operator

bitwise comparison

| **Symbol** | **Usage** | **Meaning** |
| --- | --- | --- |
| ~ | ~p | Returns negation of p |
| | | p | q | p OR q |
| & | p & q | p AND q |
| ^ | p ^ q | p XOR q (exclusive or) |

通过操作符来合并一些boolean series

`df[”column”].isin(list)` 返回一个boolean series，表示所有该栏下在list中的项

`df[”column”].str.startswith(”N”)` 返回所有以N开头的boolean series

## Adding, Removing, and Modifying Columns

`df[”new column name”]=series`

类似np，可以直接拿出一个column—做操作

`df=df.rename(columns={”old name”:”new name”})` 重命名一个column

`df.drop(”columnname”, axis=”columns”)` 返回删除一个column后的df

## Utility Functions

### NumPy

pandas数据可以直接用numpy函数。pandas中的series底层实现就是np数组

### Built-In pandas Methods

`.shape` 返回一个tuple（rows，columns）

`.size` 返回row数量*column数量

`.describe()` 返回一个dataframe或者series，包括了很多有用的信息（比如count, mean, min, 25%)

`.sample()` 随机选取一些（default返回一个，需要修改就括号里写需要几个）

`.sample(5,replace=True)` 放回抽取5个（默认不放回）

`Series.unique()` 返回所有出现元素的array（仅算一个）

`Series.value_counts()` 计算Series中每个唯一值出现的次数

`Series.sort_values()` 重新排序（index不改变，跟着移动）

`df.sort_values(by=”column”, ascending=False)` 排序dataframe

## Custom Sort

`.sort_values(”column”, key = lambda x:x…, ascending=True)`使用lambda函数+sort_values

`.map()`方法：编一个函数，用series.map(函数名)给原来的df加一个column，最后用`sort_values(by=”这个column”,ascending=False)`