# Label Encoding

```python
from sklearn import preprocessing
label_encoder = preprocessing.LabelEncoder() # Creating obj
```

``` python
label_encoder.fit(["Class 1", "Class2" ... "Class N"])
```
Fit assigns a number to each of the labels passed to it. Duplicates are handled,
ie, if there are 2 instances of 'Class9', both of them will be assigned the number 9. 9 because it is 1 indexed.

```python
encoding = label_encoder.transform(["Class 1", "Class 2", "Class 1", "Class 3"])
```

transform returns an array(numpy.array) of the encoded labels in the given list.
In the above example, the returned values are

```python 
[1, 2, 1, 4] 
```

## Warning :
* Does not play well with NaN values or missing data. 
    * Use Imputer from sklearn.preprocessing. Check individual note for more details.