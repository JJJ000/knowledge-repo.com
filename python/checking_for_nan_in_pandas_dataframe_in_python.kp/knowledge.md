---
title: How to determine if any values in a pandas dataframe are nan?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can check if any value is NaN in a Pandas DataFrame by using the isnull() or isna() methods.
---

**Contents**

[TOC]

#1 Using the isnull() Method

Pandas provides a built-in function called isnull() which can be used to detect NaN values in a dataframe. It returns a boolean value which is True if the value is NaN and False if the value is not NaN.

Example:

```
import pandas as pd

df = pd.DataFrame([[1, 2, 3], [4, 5, 6], [7, 8, 9], [None, 0, 1]])

df.isnull()
```

#2 Using the isna() Method

Pandas also provides a built-in function called isna() which can be used to detect NaN values in a dataframe. It returns a boolean value which is True if the value is NaN and False if the value is not NaN.

Example:

```
import pandas as pd

df = pd.DataFrame([[1, 2, 3], [4, 5, 6], [7, 8, 9], [None, 0, 1]])

df.isna()
```

#3 Using the notnull() Method

Pandas provides a built-in function called notnull() which can be used to detect non-NaN values in a dataframe. It returns a boolean value which is True if the value is not NaN and False if the value is NaN.

Example:

```
import pandas as pd

df = pd.DataFrame([[1, 2, 3], [4, 5, 6], [7, 8, 9], [None, 0, 1]])

df.notnull()
```

#4 Using the notna() Method

Pandas also provides a built-in function called notna() which can be used to detect non-NaN values in a dataframe. It returns a boolean value which is True if the value is not NaN and False if the value is NaN.

Example:

```
import pandas as pd

df = pd.DataFrame([[1, 2, 3], [4, 5, 6], [7, 8, 9], [None, 0, 1]])

df.notna()
```
