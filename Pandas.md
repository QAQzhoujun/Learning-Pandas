# Learning-Pandas
----------------

### `sort.values()` <br>
```python
DataFrame.sort_values(by=‘##’,axis=0,ascending=True, inplace=False, na_position=‘last’)  

by            #指定列名(axis=0或’index’)或索引值(axis=1或’columns’) 
axis          #若axis=0或’index’，则按照指定列中数据大小排序；若axis=1或’columns’，则按照指定索引中数据大小排序，默认axis=0 
ascending     #是否按指定列的数组升序排列，默认为True，即升序排列 
inplace       #是否用排序后的数据集替换原来的数据，默认为False，即不替换 
na_position   #{‘first’,‘last’}，设定缺失值的显示位置 
```

### `loc(df[''])` <br>



### `icol irow ix 选取行列` <br>
[choose row or colume](https://blog.csdn.net/wanglingli95/article/details/78887771) <br>
```python
data.ix[[1,2],[0]]   #选择第2,3行第1列的值
df3 = df2.ix[:,['upper_boundary','lower_boundary']]   #选择up和low的2列的全部行

list.sort(key = lambda x:x[--])

```
###  `data.drop 删除指定行` <br>
```python
df = df.drop(df[df.score < 50].index)
df.drop(df[df.score < 50].index, inplace=True)   #替换版本
df = df.drop(df[(df.label == -1) | (df.label ==2)].index)
```
### `data.lable.value_counts(dropna == False)` <br>
```python
data.lable.value_counts(dropna = False)
```

### `选取特定列并调节title顺序`<br>
```python
df = df.ix[:,['upper_boundary','lower_boundary']]
p_col = ['up','low']
df.columns = p_col
```
