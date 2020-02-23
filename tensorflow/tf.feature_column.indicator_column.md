Represents multi-hot representation of given categorical column.
```python
tf.feature_column.indicator_column(categorical_column)
```

Args:
```categorical_column```: A ```CategoricalColumn``` which is created by ```categorical_column_with_*``` or ```crossed_column``` functions.
Returns:
An ```IndicatorColumn```.
