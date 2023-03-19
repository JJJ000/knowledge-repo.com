---
title: How to display an entire lengthy string in a pandas data table?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Set the option to display the maximum number of characters using pandas.options.display.max\_colwidth = -1.
---

**Contents**

[TOC]

Introduction: 

While working with data in python, we often come across long strings which needs to be displayed completely in the pandas data frame. By default, pandas only displays a part of the string and replace the rest of the string by '...'. In this article, we will learn how to print very long string completely in pandas dataframe in Python.


Section 1: Increase the display width of Pandas Data Frame

The first step to print long string completely in pandas dataframe is to increase the display width of the pandas data frame. It can be done using the `set_option()` method of pandas. The `set_option()` method allows us to set different options related to the display. The code block to increase the display width is:

```python
# import pandas library
import pandas as pd

# increase the display width
pd.set_option('display.max_colwidth', -1)
```

The above code will increase the display width of pandas data frame and set the option to display long string completely in pandas data frame.


Section 2: Create a sample data frame with long strings

To test the above code, let's create a sample pandas data frame with long strings. The code is given below:

```python
# create a sample data frame with long strings
df = pd.DataFrame({'Column1': ['This is a very long string which needs to be displayed completely in the pandas data frame', 'Another very long string which also needs to be displayed completely in the pandas data frame']})
```

The above code will create a sample data frame with two rows and one column.


Section 3: Display the sample data frame

Now that we have increased the display width of pandas data frame and created a sample data frame with long strings, we can display the data frame using the `print()` function. The code to display the sample data frame is given below:

```python
#display the data frame
print(df)
```

The above code will display the complete long strings in the pandas data frame.


Section 4: Complete code

The complete code to print very long string completely in pandas dataframe is given below:

```python
# import pandas library
import pandas as pd

# increase the display width
pd.set_option('display.max_colwidth', -1)

# create a sample data frame with long strings
df = pd.DataFrame({'Column1': ['This is a very long string which needs to be displayed completely in the pandas data frame', 'Another very long string which also needs to be displayed completely in the pandas data frame']})

# display the data frame
print(df)
```

The above code will import pandas library, increase the display width, create a sample pandas data frame with long strings, display the data frame with complete long strings in pandas data frame.
