# Table Of Content

[1st pandas Notbook](#1st-pandas-notbook)

[How tp find pd virson](#how-tp-find-pd-virson)

[Make data Frame using Pandas](#make-data-frame-using-pandas)

[Npy array use to create data frame](#npy-array-use-to-create-data-frame)

[Numpy array of randm no datafarm](#numpy-array-of-randm-no-datafarm)

[How to rename colum](#how-to-rename-colum)

[To replace any strng and thng in clmn name](#to-replace-any-strng-and-thng-in-clmn-name)

[To add prefix](#to-add-prefix)

[To add suffix](#to-add-suffix)

[Usnig templet](#usnig-templet)

# 1st pandas Notbook

## how tp find pd virson

```python
import pandas as pd
pd.__version__
```

This will give you the version of pandas that is installed on your system. You can also check this by running `!pip show pandas` in

## Make data Frame using Pandas

```python
df=pd.DataFrame({'A col':[1,2,3,4,5] , 'B col': ['Ahmed','Qasm','Amjad','Amjad','Amjad']})
df.head

```

## npy array use to create data frame

```python
import numpy as np
arr=np.array([[1,2,3],[4,4,5],[6,5,8]])
arr
df=pd.DataFrame(arr)
```

## numpy array of randm no datafarm

```python
pd.DataFrame(np.random.rand(4,5))
pd.DataFrame(np.random.rand(5,51) )   
```

## how to rename colum

```python
df=pd.DataFrame({'A col':[1,2,3,4,5] , 'B col': ['Ahmed','Qasm','Amjad','Amjad','Amjad']})
df.rename(columns={'A col':'a ', 'B col':'b' },inplace=True)
df
df.columns=['aa','bb']
df
```

## to replace any strng and thng in clmn name

```python
df.columns=df.columns.str.replace('a','A') 
df
```

### to add prefix

```python
df=df.add_prefix('blal')
df
```

### to add suffix

```python
#to add suffix
df=df.add_suffix('blal')
df
df.columns=['col2','col2']
df
```

## usnig templet

```python
mport pandas as pd
import numpy as np
import seaborn as sns
phool=sns.load_dataset('tips')
phool.head(10)
phool.describe()
phool.columns
#save a dataset
phool.to_csv('tips_sa2.csv')
phool.to_excel('tips_sas.xlsx')
#to import data set
r=pd.read_excel('tips_sas.xlsx')
r.head(10) 
```
