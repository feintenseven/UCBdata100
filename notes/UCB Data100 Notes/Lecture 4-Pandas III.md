# Lecture 4-Pnadas III

Summary: Grouping, Pivot Table, Joining Tables

## Grouping

`.groupby(”column”)` 根据该column来分组为subframe（sf）

`.groupby([”co1”,”co2”])` 返回multi-index df

`.agg()` 对sf内数据做处理 

**eg.`babynames.groupby("Year")[["Count"]].agg("sum")`**

![image.png](Lecture%204-Pandas%20III/image.png)

![image.png](Lecture%204-Pandas%20III/image%201.png)

注意：像agg(max)这些，是每组sf内每个column分开筛选的！row的部分之间的被打乱了

`.groupby().size()` 返回每组行数(series)

`.groupby().count()` 返回每组每列非空的数量(可能是df)

`.groupby().filter(lambda sf:sf…)` 用于sf筛选，返回通过筛选的sf组成的df

## Pivot Table

数据透视表，双索引（纵横）

![image.png](Lecture%204-Pandas%20III/image%202.png)

## Joining Tables

`pd.merge(left=df1, right=df2, left_on=”the column name of left”, right_on=”the column name of right”)`

“on”的就是拼接的中介（决定哪一行拼哪一行，也就是只有left_on=right_on的部分会拼到一起）

或者：

`df1.merge( right=df2, left_on=”the column name of left”, right_on=”the column name of right”)`