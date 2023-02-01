---
title: Transform a pandas dataframe into a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The pandas dataframe can be converted to a NumPy array using the .values attribute.
---

**Contents**

[TOC]

# Section 1: Importing Necessary Libraries

We need to import the necessary libraries before we can convert a pandas dataframe to a NumPy array.

```python
import numpy as np
import pandas as pd
```

# Section 2: Creating a Pandas DataFrame

We can create a pandas dataframe from a dictionary of lists. 

```python
data = {'Name':['John', 'Paul', 'George', 'Ringo'],
        'Age':[21, 22, 23, 24],
        'Height':[180, 182, 172, 174]}

df = pd.DataFrame(data)
```

# Section 3: Converting to a NumPy Array

We can convert the pandas dataframe to a NumPy array using the `.values` attribute.

```python
np_array = df.values
```

# Section 4: Verifying the Conversion

We can verify the conversion by checking the type of the object.

```python
type(np_array)
```

Output: `numpy.ndarray`
