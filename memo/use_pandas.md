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

## キーで結合
```python
pd.merge(data1, data2, left_on='KEY', right_on='KEY')
```

## 特定の行の抜き出し
data.columnに'sample'が入っている行だけ抜き出す
```python
data[data.column == 'sample']
```

## カラムの順番を入れ替える
```python
data.ix[:,[1,3,2]]
```

## ヒストグラムのプロット
```python
data.col.plot.hist(bins=100)
```

## 基本的な統計量の出力
```python
data.col.describe()
```

### 出力される項目の詳細
* count
データ数
* mean
平均
* std
標準偏差  
データのばらつきを指標
* min, 25%, 50%, 75%, max
min, max は最小値, 最大値  
25%, 50%, 75% は25%番目, 50%番目(中央値), 75%番目の値

## 要約した値の可視化(箱ひげ図)
```python
data.col.boxplot()
```

## pandasの配列をnumpyの配列に変換する
```python
npdata = np.array(data.col)
```
