---
title: Randomize the order of the rows in the dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Shuffle the rows of a DataFrame in Python by using the sample() method on the DataFrame.
---

**Contents**

[TOC]

##### Using `sample()`

The `sample()` function in Pandas can be used to shuffle the rows of a DataFrame. To use the `sample()` function, you will need to specify the `frac` parameter to indicate the fraction of rows that should be returned in the shuffled DataFrame.

```
# Shuffle DataFrame rows
df = df.sample(frac=1)
```

##### Using `np.random.permutation()`

Another way to shuffle DataFrame rows is to use the `np.random.permutation()` function from the NumPy library. This function will generate a random permutation of the indices of the DataFrame, which can then be used to reorder the rows.

```
# Generate a random permutation of indices
perm = np.random.permutation(df.index)

# Reorder DataFrame rows
df = df.loc[perm]
```

##### Using `np.random.shuffle()`

The `np.random.shuffle()` function from the NumPy library can also be used to shuffle the rows of a DataFrame. This function takes a list of indices as an argument and shuffles them in place.

```
# Generate a list of indices
indices = df.index.tolist()

# Shuffle the indices
np.random.shuffle(indices)

# Reorder DataFrame rows
df = df.loc[indices]
```

##### Using `np.random.choice()`

The `np.random.choice()` function from the NumPy library can also be used to shuffle the rows of a DataFrame. This function takes a list of indices as an argument and randomly selects a subset of them.

```
# Generate a list of indices
indices = df.index.tolist()

# Randomly select a subset of the indices
indices = np.random.choice(indices, size=len(indices), replace=False)

# Reorder DataFrame rows
df = df.loc[indices]
```
