# Lecture 2-Pandas I

Summary: DataFrames, Series, Indices, Extracting data

## DataFrames, Series, and Indices

DataFrame a collection of Series that all share the same Index

创建dataframe：

`pd.DataFrame(data,index,columns)`

- 从CSV导入：

`pd.read_csv(文件路径)`

- 用list和column names

`pd.DataFrame([1,2,3],columns=[”Numbers”])`

![image.png](Lecture%202-Pandas%20I/image.png)

`pd.DataFrame([[1,”one”], [2,”two”]], columns = [”Number”, “Description])`

![image.png](Lecture%202-Pandas%20I/image%201.png)

- 用python字典

行/列两种方式

![image.png](Lecture%202-Pandas%20I/image%202.png)

- 用Series

![image.png](Lecture%202-Pandas%20I/image%203.png)

### Index

可以是非数字，可以重复

`dafra.set_index(”column name”)` 改变index列

`dadra.reset_index()` 恢复default index（0 1 2…）

`dafra.index` 返回所有index

`dafra.columns` 返回所有column名字（不包括index）

`dafra.shape` 返回（总行数，总列数）

## Extracting Data

`df.head(n)` 截取前n行（index）

`df.tail(n)` 截取后n行（index）

`df.loc[row_labels, column_labels]` 返回该row-column下的内容，可以是list，df slice或者single value（row和column可以是array或者a:b（从a到b，包括a和b），：（所有））

![如果column不用[ ]框起来，就会返回series](Lecture%202-Pandas%20I/image%204.png)

如果column不用[ ]框起来，就会返回series

`df.iloc[row_int, column_int]` 通过整数索引找到

`[]` 1 a slice of row number a:b不能是单个数字

2 a list of column labels

3 a single column label