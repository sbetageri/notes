# One Hot Encoding

> #### Data
``` csv
label1,label2,label3
A,B,C
C,A,B
B,C,A
A,B,C
C,A,B
B,C,A
A,B,C
C,A,B
B,C,A
A,B,C
C,A,B
B,C,A
A,B,C
C,A,B
B,C,A
```

> #### Output

```python
One Hot Encoding
[[ 1.  0.  0.]
 [ 0.  0.  1.]
 [ 0.  1.  0.]
 [ 1.  0.  0.]
 [ 0.  0.  1.]
 [ 0.  1.  0.]
 [ 1.  0.  0.]
 [ 0.  0.  1.]
 [ 0.  1.  0.]
 [ 1.  0.  0.]
 [ 0.  0.  1.]
 [ 0.  1.  0.]
 [ 1.  0.  0.]
 [ 0.  0.  1.]
 [ 0.  1.  0.]]

```

> #### Code

```python
import numpy as np
import pandas as pd
from sklearn import preprocessing

df = pd.read_csv('./one_hot_encoding_data.csv')

label_encoder = preprocessing.LabelEncoder()
label_encoder.fit(['A', 'B', 'C'])

df['label1'] = label_encoder.transform(df['label1'])

print("One Hot Encoding")
one_hot_encoder = preprocessing.OneHotEncoder()
one_hot_encoder.fit([9, 9, 9])
# The above statement is always tricky. Not at all sure how it works.
# Just know that 

tr = one_hot_encoder.transform(df[['label1']]).toarray()
# We pass df[['label1']], ie, the parameter as a list
# reason is that df[[val]] returns a dataframe that is used
# by the one hot encoder. 

print(tr)
```