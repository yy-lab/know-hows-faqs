# Tips and Tricks

## Workflow and IU supercomputers

- [Recording](https://iu.mediaspace.kaltura.com/media/t/1_dr5mq1ek)
- [Demo repo](https://github.com/yangkcatiu/workflowdemo)

## Python

```python
numerical_group_ids = np.unique(group_ids, return_inverse=True)[1]
```

converts an array of strings (or integers) to an array of numerical IDs, where the same strings have the same IDs.
