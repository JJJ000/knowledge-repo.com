---
title: What is the solution for the 'object arrays cannot be loaded when allow_pickle=false' error in the imdb.load_data() function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Set the allow\_pickle parameter to True when using the imdb.load\_data() function in Python.
---

**Contents**

[TOC]

# Problem Overview
The error `Object arrays cannot be loaded when allow_pickle=False` occurs when `allow_pickle` argument of `np.load()` function is set `False` while loading an object array. This error can also occur when you are trying to load data from a file which has been saved with `allow_pickle=False`. 

In the context of this question, this error is encountered when trying to load data using `imdb.load_data()` function from the Keras library. 

In this guide, we will discuss the possible reasons for this error and ways to fix it.

# Solution

## Modify the load_data() function
One of the ways to fix the error is to edit the `imdb.load_data()` function. We need to add `allow_pickle=True` as an argument when loading the data using `np.load()`. Here's how we can do that.

```python
def load_data(path='imdb.npz', num_words=None, skip_top=0, maxlen=None, seed=113, start_char=1, oov_char=2, index_from=3):
    if '://' in path:
        path = get_file(fname=path, origin=path,
                        file_hash='599dadb1135973df5b59232a0e9a887c')
    with np.load(path, allow_pickle=True) as f:
        x_train, labels_train = f['x_train'], f['y_train']
        x_test, labels_test = f['x_test'], f['y_test']
    np.random.seed(seed)
    indices = np.arange(len(x_train))
    np.random.shuffle(indices)
    x_train = x_train[indices]
    labels_train = labels_train[indices]
    indices = np.arange(len(x_test))
    np.random.shuffle(indices)
    x_test = x_test[indices]
    labels_test = labels_test[indices]
    xs = np.concatenate([x_train, x_test])
    labels = np.concatenate([labels_train, labels_test])
    if start_char is not None:
        xs = [[start_char] + [w + index_from for w in x] for x in xs]
    elif index_from:
        xs = [[w + index_from for w in x] for x in xs]
    if maxlen:
        xs, labels = _remove_long_seq(maxlen, xs, labels)
        if not xs:
            raise ValueError('After filtering for sequences shorter than maxlen=' +
                             str(maxlen) + ', no sequence was kept. '
                             'Increase maxlen.')
    if not num_words:
        num_words = max([max(x) for x in xs])
    if oov_char is not None:
        xs = [[w if (skip_top <= w < num_words) else oov_char for w in x] for x in xs]
    else:
        xs = [[w for w in x if skip_top <= w < num_words] for x in xs]
    idx = len(x_train)
    x_train, y_train = np.array(xs[:idx]), np.array(labels[:idx])
    x_test, y_test = np.array(xs[idx:]), np.array(labels[idx:])
    return (x_train, y_train), (x_test, y_test)
```

After making the changes, you can now load the data using the newly modified function.

```python
from keras.datasets import imdb

(x_train, y_train), (x_test, y_test) = imdb.load_data()
```

## Save the data with allow_pickle=True
If modifying the `load_data()` function is not an option, you can save the data with `allow_pickle=True`. Here's how you can do that.

```python
import numpy as np
from keras.datasets import imdb

(x_train, y_train), (x_test, y_test) = imdb.load_data()

np.savez('imdb_data.npz', x_train=x_train, y_train=y_train, x_test=x_test, y_test=y_test, allow_pickle=True)
```

After saving the data, you can load it as follows.

```python
data = np.load('imdb_data.npz', allow_pickle=True)

x_train, y_train = data['x_train'], data['y_train']
x_test, y_test = data['x_test'], data['y_test']
```

## Upgrade to numpy 1.16 or later
If you are using numpy version older than 1.16, it's possible that you may encounter this error. The `allow_pickle` argument was introduced in version 1.16, so upgrading to the latest version of numpy can resolve the issue. You can upgrade to the latest version of numpy by running the following command.

```
!pip install numpy --upgrade
```

After upgrading numpy, you can load the data as follows.

```python
from keras.datasets import imdb

(x_train, y_train), (x_test, y_test) = imdb.load_data()
```

# Conclusion
In this guide, we discussed the error `Object arrays cannot be loaded when allow_pickle=False`, which can occur when loading an object array with `allow_pickle=False`. We provided three ways to fix this error - modifying the `load_data()` function, saving the data with `allow_pickle=True`, and upgrading to the latest version of numpy.
