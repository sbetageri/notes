# Filling missing data

By using pandas, we can fill missing data using:

``` python
dataframe = dataframe.fillna('<value>')
```

Even
``` python
dataframe['Feature'] = dataframe['Feature'].fillna('<value>')
```
