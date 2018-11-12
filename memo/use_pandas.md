# pandas でデータの前処理を行う

pandasのインポートを行う
```python
import pandas as pd
```

## csv の読込
```python
data = pd.read_csv('file name')
```

## csv の出力
```python
data.to_csv('file name')

## csv の 中身をみる
```python
data.head()
# 100行分みたいとき
data.head(100)
```
## 行数を確認
```python
print(len(data))
```
## 列数の確認
```python
print(len(data.columns))
```

## 欠損値(NaN)の除外
### 欠損値がある行を除く
```python
data.dropna()
```

### 欠損値がある列を除く
```python
data.dropna(axis=1)
```

## Index値のリセット
reset_index()

## 不要列の削除
```python
drop_col = ['col1', 'col2', 'col3']
data.drop(drop_col, axis=1)
```

## 表の結合
```python
pd.concat = (
    [data1,
     data2,
     data3],
     axis=1
     )
```
