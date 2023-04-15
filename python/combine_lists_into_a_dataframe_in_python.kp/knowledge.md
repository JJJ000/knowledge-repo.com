---
title: Convert several lists into a dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To convert multiple lists into a dataframe in Python, you can use the pandas library and its DataFrame function.
---

**Contents**

[TOC]

## Section 1: Creating Lists

First, we need to create the lists that we will be using to create the dataframe. We can create multiple lists of different lengths and types, depending on the data that we want to represent in our dataframe. For example:

```
ages = [25, 30, 35, 40, 45]
names = ['John', 'Jane', 'Bob', 'Lisa', 'Tom']
salaries = [50000, 60000, 70000, 80000, 90000]
```

Here, we have three lists: `ages`, `names`, and `salaries`. The `ages` list contains integers, the `names` list contains strings, and the `salaries` list contains integers. We will use these lists to create a dataframe that will represent the data in a tabular format.


## Section 2: Importing pandas and Creating Dataframe

Next, we need to import the pandas library, which is a popular library for data manipulation and analysis in Python. We can import pandas using the following line of code:

```
import pandas as pd
```

Once we have imported pandas, we can create a dataframe by passing our lists as arguments to the pandas `DataFrame()` function. Here is an example code:

```
import pandas as pd

ages = [25, 30, 35, 40, 45]
names = ['John', 'Jane', 'Bob', 'Lisa', 'Tom']
salaries = [50000, 60000, 70000, 80000, 90000]

df = pd.DataFrame({'Name': names, 'Age': ages, 'Salary': salaries})
```

In this code, we are passing our lists `ages`, `names`, and `salaries` to the `DataFrame()` function as a dictionary. The keys of the dictionary are the column names that we want to use in our dataframe. In this example, we are using 'Name', 'Age', and 'Salary' as our column names. The values of the dictionary are the lists that we defined earlier. The `pd.DataFrame()` function creates a new dataframe and assigns it to the variable `df`.


## Section 3: Displaying Dataframe

Finally, we can display our dataframe by simply printing the variable `df`. Here is an example code:

```
import pandas as pd

ages = [25, 30, 35, 40, 45]
names = ['John', 'Jane', 'Bob', 'Lisa', 'Tom']
salaries = [50000, 60000, 70000, 80000, 90000]

df = pd.DataFrame({'Name': names, 'Age': ages, 'Salary': salaries})

print(df)
```

When we run this code, the output will be a tabular format of our data in the dataframe. It should look like this:

```
   Name  Age  Salary
0  John   25   50000
1  Jane   30   60000
2   Bob   35   70000
3  Lisa   40   80000
4   Tom   45   90000
```

Here, the dataframe has three columns: 'Name', 'Age', and 'Salary'. Each row represents an individual record in our data, and the values in each row represent the corresponding values of that record's columns.
