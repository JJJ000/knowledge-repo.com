---
title: What is the process to generate a dataframe consisting of random integers using pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the pandas.DataFrame() function with the numpy.random.randint() function to create random integers and specify the shape of the DataFrame.
---

**Contents**

[TOC]

Header: Pandas

Pandas is a popular data manipulation library for Python. It provides data structures and tools for working with structured data, and is widely used for data analysis and modeling.

Section 1: Generating a DataFrame of Random Integers

To generate a DataFrame of random integers, we can use the `pandas.DataFrame` function and pass in a numpy array of random integers. We can use the `numpy.random.randint()` function to generate an array of random integers.

```
import pandas as pd
import numpy as np

data = np.random.randint(low=0, high=100, size=(5, 4))
df = pd.DataFrame(data, columns=['col1', 'col2', 'col3', 'col4'])
print(df)
```

In this example, we generated a 5 by 4 array of random integers between 0 and 100, and created a DataFrame with column names 'col1', 'col2', 'col3', and 'col4'. We then printed the resulting DataFrame to the console.

Section 2: Specifying the Index

By default, the `pandas.DataFrame` function generates a range index starting from 0. However, we can also specify the index for the DataFrame using the `index` parameter.

```
import pandas as pd
import numpy as np

data = np.random.randint(low=0, high=100, size=(5, 4))
df = pd.DataFrame(data, columns=['col1', 'col2', 'col3', 'col4'], index=['row1', 'row2', 'row3', 'row4', 'row5'])
print(df)
```

In this example, we specified an index of 'row1' through 'row5'. The resulting DataFrame will have the specified index instead of the default range index.

Section 3: Generating a DataFrame of Random Floats

To generate a DataFrame of random floats, we can follow a similar approach as we did with random integers. We can use the `numpy.random.rand()` function to generate an array of random floats between 0 and 1.

```
import pandas as pd
import numpy as np

data = np.random.rand(5, 4)
df = pd.DataFrame(data, columns=['col1', 'col2', 'col3', 'col4'])
print(df)
```

In this example, we generated a 5 by 4 array of random floats between 0 and 1, and created a DataFrame with column names 'col1', 'col2', 'col3', and 'col4'. We then printed the resulting DataFrame to the console.
