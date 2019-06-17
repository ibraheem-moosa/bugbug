# Bug Description

The goal of this document is to provide descriptions of all the bug features.
It will help us in feature engineering and data preprocessing.

Each line in `bugs.json` correspons to a bug. The number of bugs in `bugs.json` can be
easily determined by `wc -l bugs.json`. Currently this number is `127958`.

The bugs are in json format. This means each bug is a collection of key-value
pairs. The keys can be thought of as feature names and the values are feature
values. You can easily read the bugs using python's json library.
```python
with open('bugs.json') as f:
	bugs = [json.loads(l) for l in f]
```

Be careful. If you do not have at least 8gb ram you will run out of memory.

Not all keys/features are present in all bugs. `66` keys are present in all
the bugs.

```python
commonkeys = set.intersection(*(set(b.keys()) for b in bugs))
print(len(commonkeys))
```

There `272` different keys.
```python
allkeys = set.union(*(set(b.keys()) for b in bugs))
print(len(allkeys))
```

Description of all these will be provided.

