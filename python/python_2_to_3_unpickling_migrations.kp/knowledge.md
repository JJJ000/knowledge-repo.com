---
title: Converting a pickled Python 2 object to Python 3 format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: Python 3 can unpickle a Python 2 object if the protocol used is compatible and if the necessary Python 2 modules are available in the Python 3 environment.
---

**Contents**

[TOC]

Introduction
------------

When pickling a Python object, you are essentially converting it into a format that can be stored or transmitted. Unpickling is the reverse process of loading the pickled object. Python 2 and Python 3 have different ways of pickling and unpickling objects, which makes it challenging when using pickled data across different Python versions. The following sections will show you how to unpickle a Python 2 object with Python 3.

Use the 'pickle' module
-----------------------

The `pickle` module provides the functionality for serializing and deserializing Python objects. To unpickle a Python 2 object with Python 3, you can use the `pickle.load()` method to load the pickled data into a Python 3 object. Here's an example:

```python
import pickle

# Load the pickled data from file
with open('mypickleddata.pkl', 'rb') as f:
    data = f.read()

# Unpickle the data
myobj = pickle.loads(data, encoding='latin1')
```

You need to pass an `encoding` parameter to the `loads()` method to specify the encoding that was used when pickling the object. The `latin1` encoding is an excellent choice because it can handle all 256 characters in the Latin-1 character set.

Use the 'six' module
--------------------

The ‘six’ module provides simple utilities for wrapping over differences between Python 2 and Python 3. The `six.moves.cPickle` module provides a drop-in replacement for the `pickle` module. To unpickle a Python 2 object with Python 3, you can use the `six.moves.cPickle` module instead of the `pickle` module. Here's an example:

```python
import six.moves.cPickle as pickle

# Load the pickled data from file
with open('mypickleddata.pkl', 'rb') as f:
    data = f.read()

# Unpickle the data
myobj = pickle.loads(data)
```

`six.moves.cPickle` provides the same functionalities as `pickle` but uses the C implementation of the Pickle protocol, which can be faster than the pure Python implementation used by `pickle`.

Use the 'dill' module
--------------------

The `dill` module is a third-party module that extends the functionality of the built-in `pickle` module. It can serialize a broader range of Python objects than `pickle`, including traceback objects, lambdas, instances of nested classes, and self-referential objects. Additionally, `dill` can handle functions defined interactively or as strings.

To unpickle a Python 2 object with Python 3 using `dill`, you can use the `dill.load()` method to load the pickled data into a Python 3 object. Here's an example:

```python
import dill

# Load the pickled data from file
with open('mypickleddata.pkl', 'rb') as f:
    data = f.read()

# Unpickle the data
myobj = dill.loads(data)
```

`dill` works with Python 3 by using the `pickles` module from Python 2 as a reference implementation. You don't need to specify an encoding parameter when using `dill`.

Conclusion
----------

When working with pickled data across different Python versions, it's essential to choose the right approach. You can use the built-in `pickle` module with a specific encoding parameter or use `six.moves.cPickle` module for compatibility between Python 2 and 3. Additionally, you can use the third-party module `dill` to handle more complex objects. When unpickling a Python 2 object with Python 3, be careful to use the appropriate approach to avoid errors.
