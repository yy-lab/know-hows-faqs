# Tips and Tricks

## Python

```python
numerical_group_ids = np.unique(group_ids, return_inverse=True)[1]
```

converts an array of strings (or integers) to an array of numerical IDs, where the same strings have the same IDs.