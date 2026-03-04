# Lecture 5-Data Wrangling and EDA

Summary: Reading Files, Variables

## Reading CSVs

`pd.read_csv(”路径”, head=从第几行开始读)`

## Reading JSONs

json是一个python字典

```python
import json
with open(congress_file, "rb") as f:
congress_json = json.load(f)
```

## Rectangular Data

Tables(DataFrame in R/Python), Matrices

## Variable

quantitative 定量

qualitative定性 —ordinal定序 nominal定类

`pd.to_daytime(,format='%m/...')` 转化为时间

`series.dt.month` 返回月份（series储存daytime object）