---
title: Rewording formatting a pandas dataframe for better appearance
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To pretty print a pandas dataframe in Python, use the `print` function with the dataframe as an argument or use the `to\_string` method with formatting options.
---

**Contents**

[TOC]

# Introduction

When working with pandas dataframes in Python, it is often necessary to print out the data in a human-readable format. This is commonly referred to as pretty printing. There are several ways to achieve this in pandas, and in this article, we will explore some of the most common and effective methods.

# Method 1: Using the .to_string() method

One of the simplest ways to pretty print a dataframe in pandas is to use the `.to_string()` method. This method converts the dataframe to a formatted string, which can then be printed to the console or saved to a file.

Here is an example:

```
import pandas as pd

data = {'Name': ['John', 'Megan', 'Derek', 'Kate'],
        'Age': [25, 32, 18, 47],
        'City': ['New York', 'Chicago', 'Los Angeles', 'Houston']}

df = pd.DataFrame(data)

print(df.to_string(index=False))
```

In this example, we are creating a simple dataframe with three columns - Name, Age, and City. We then print the dataframe to the console using the `to_string()` method, which includes all rows and columns without an index.

# Method 2: Using the .style property

Another way to pretty print a dataframe in pandas is to use the `.style` property. This property allows us to apply various formatting options to the dataframe, such as highlighting cells, setting font size and color, and more.

Here is an example:

```
import pandas as pd

data = {'Name': ['John', 'Megan', 'Derek', 'Kate'],
        'Age': [25, 32, 18, 47],
        'City': ['New York', 'Chicago', 'Los Angeles', 'Houston']}

df = pd.DataFrame(data)

styled_df = df.style.set_properties(**{'text-align': 'center'})

print(styled_df)
```

In this example, we are creating a simple dataframe with three columns - Name, Age, and City. We then create a new variable `styled_df` which contains the formatted dataframe using the `.style` property. In this case, we are setting the text alignment of all cells to center using the `set_properties()` method.

# Method 3: Using the .to_html() method

A third way to pretty print a dataframe in pandas is to use the `.to_html()` method. This method converts the dataframe to an HTML string, which can then be inserted into an HTML document or displayed in a Jupyter Notebook.

Here is an example:

```
import pandas as pd

data = {'Name': ['John', 'Megan', 'Derek', 'Kate'],
        'Age': [25, 32, 18, 47],
        'City': ['New York', 'Chicago', 'Los Angeles', 'Houston']}

df = pd.DataFrame(data)

html_table = df.to_html(index=False)

print(html_table)
```

In this example, we are creating a simple dataframe with three columns - Name, Age, and City. We then use the `.to_html()` method to convert the dataframe to an HTML string and assign it to the variable `html_table`. We then print this variable to the console.

# Conclusion

There are several effective ways to pretty print a pandas dataframe in Python. The .to_string(), .style, and .to_html() methods provide different formatting options that can help to make the data more readable and visually appealing. Consider trying different methods to find the best one for your specific use case.
