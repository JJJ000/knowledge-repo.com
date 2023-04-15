---
title: Restructure a list into a column of a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To convert a list to a Pandas dataframe column in Python, use the following code df[`column\_name`] = pd.Series(list\_name).
---

**Contents**

[TOC]

## Convert List to Pandas Dataframe Column

The process of converting a list to a dataframe column in Python is a common and essential operation in data analysis. The following are some ways to achieve this with Pandas.

### Method 1: Using the DataFrame constructor

One way to convert a list to a dataframe column is by using the DataFrame constructor. In this method, we create a new dataframe and append the list as a column. Here is an example code to achieve this:

```python
import pandas as pd

# create the list
my_list = [1, 2, 3, 4]

# create the dataframe and add the column
df = pd.DataFrame()
df['My_Column'] = my_list

print(df)
```

The output will be:

```
   My_Column
0          1
1          2
2          3
3          4
```

### Method 2: Using the assign() method

Another way to add a column to a dataframe is by using the assign() method. This method creates a new column by applying a function to an existing column or by creating a new series from a list or array. Here is an example code to achieve this:

```python
import pandas as pd

# create the list
my_list = [1, 2, 3, 4]

# create the dataframe
df = pd.DataFrame({'A': [10, 20, 30, 40], 'B': [100, 200, 300, 400]})

# assign the list as a new column
df = df.assign(My_Column=my_list)

print(df)
```

The output will be:

```
    A    B  My_Column
0  10  100          1
1  20  200          2
2  30  300          3
3  40  400          4
```

### Method 3: Using insert() method

We can also use the insert() method to add a new column to a dataframe at a specific index. Here is an example code to achieve this:

```python
import pandas as pd

# create the list
my_list = [1, 2, 3, 4]

# create the dataframe
df = pd.DataFrame({'A': [10, 20, 30, 40], 'B': [100, 200, 300, 400]})

# insert the list as a new column in index 1
df.insert(loc=1, column='My_Column', value=my_list)

print(df)
```

The output will be:

```
    A  My_Column    B
0  10          1  100
1  20          2  200
2  30          3  300
3  40          4  400
```

### Method 4: Using Series()

We can also convert a list to a Pandas Series and then add it as a new column to a dataframe using the concat() method. Here is an example code to achieve this:

```python
import pandas as pd

# create the list
my_list = [1, 2, 3, 4]

# create the dataframe
df = pd.DataFrame({'A': [10, 20, 30, 40], 'B': [100, 200, 300, 400]})

# convert the list to a Pandas series
my_series = pd.Series(my_list)

# concatenate the series to the dataframe
df = pd.concat([df, my_series], axis=1)

print(df)
```

The output will be:

```
    A    B  0
0  10  100  1
1  20  200  2
2  30  300  3
3  40  400  4
```

In this example, the name of the newly created column is the default name '0'. You can modify the name of the column by assigning a name after creating the series.

```python
import pandas as pd

# create the list
my_list = [1, 2, 3, 4]

# create the dataframe
df = pd.DataFrame({'A': [10, 20, 30, 40], 'B': [100, 200, 300, 400]})

# convert the list to a Pandas series with a name
my_series = pd.Series(my_list, name='My_Column')

# concatenate the series to the dataframe
df = pd.concat([df, my_series], axis=1)

print(df)
```

The output will be:

```
    A    B  My_Column
0  10  100          1
1  20  200          2
2  30  300          3
3  40  400          4
```

## Conclusion

In this tutorial, we have seen four different ways to convert a list to a Pandas dataframe column in Python. Each method is useful in different scenarios, so it's good to be familiar with all of them.
