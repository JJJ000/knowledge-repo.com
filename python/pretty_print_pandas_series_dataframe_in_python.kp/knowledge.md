---
title: Print the entire pandas series / dataframe in an aesthetically pleasing format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To pretty-print a Pandas Series/DataFrame, use the DataFrame.style.set\_properties() method.
---

**Contents**

[TOC]

**Section 1: Using the pprint() Method**

The simplest way to pretty-print an entire Pandas Series or DataFrame in Python is to use the `pprint()` method. This method takes a single argument, which is the Pandas Series or DataFrame that you want to pretty-print. For example, if you have a Pandas Series called `s`:

```python
import pandas as pd
s = pd.Series([1,2,3,4,5])

# Pretty-print the series
pprint(s)
```

The output would look like this:

```
0    1
1    2
2    3
3    4
4    5
dtype: int64
```

**Section 2: Using the to_string() Method**

Another way to pretty-print an entire Pandas Series or DataFrame in Python is to use the `to_string()` method. This method takes two optional arguments: `index` and `columns`. The `index` argument is a boolean value that determines whether or not to include the index of the DataFrame in the output. The `columns` argument is a boolean value that determines whether or not to include the columns of the DataFrame in the output. For example, if you have a Pandas DataFrame called `df`:

```python
import pandas as pd
df = pd.DataFrame({'A':[1,2,3], 'B':[4,5,6]})

# Pretty-print the dataframe
df.to_string(index=False, columns=True)
```

The output would look like this:

```
A  B
1  4
2  5
3  6
```

**Section 3: Using the Styler Object**

A third way to pretty-print an entire Pandas Series or DataFrame in Python is to use the `Styler` object. The `Styler` object is a special object that allows you to customize the look and feel of your DataFrame. This object has several methods that can be used to customize the look and feel of your DataFrame. For example, the `set_table_styles()` method can be used to set the style of the table, the `set_properties()` method can be used to set the properties of the table, and the `highlight_max()` method can be used to highlight the maximum value in the table. For example, if you have a Pandas DataFrame called `df`:

```python
import pandas as pd
df = pd.DataFrame({'A':[1,2,3], 'B':[4,5,6]})

# Pretty-print the dataframe
styler = df.style.set_table_styles([{'selector': 'th', 'props': [('background-color', '#f2f2f2')]}])
styler.highlight_max()
```

The output would look like this:

<table>
  <thead>
    <tr style="background-color: #f2f2f2;">
      <th>A</th>
      <th>B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <td>2</td>
      <td>5</td>
    </tr>
    <tr style="background-color: #ffcccc;">
      <td>3</td>
      <td>6</td>
    </tr>
  </tbody>
</table>

**Section 4: Using the HTML Output**

The fourth way to pretty-print an entire Pandas Series or DataFrame in Python is to use the HTML output. This method takes a single argument, which is the Pandas Series or DataFrame that you want to pretty-print. For example, if you have a Pandas DataFrame called `df`:

```python
import pandas as pd
df = pd.DataFrame({'A':[1,2,3], 'B':[4,5,6]})

# Pretty-print the dataframe
df.to_html()
```

The output would look like this:

```html
<table border="1" class="dataframe">
  <thead>
    <
