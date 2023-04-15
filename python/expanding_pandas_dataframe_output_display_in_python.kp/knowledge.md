---
title: What is the best way to view additional columns of a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can use the pandas DataFrame`s `set\_option` method to increase the number of columns displayed.
---

**Contents**

[TOC]

##### Using Pandas head() and tail()
The head() and tail() functions in Pandas allow you to view the first and last few rows of a DataFrame, respectively. By default, these functions will display the first five and last five rows, respectively. However, you can specify the number of rows you would like to view by passing an integer as an argument to the functions. For example, if you wanted to view the first 10 rows of a DataFrame you could use the head() function like this:

```
df.head(10)
```

##### Using Pandas display.max_columns
You can also use the pandas.set_option() function to control the number of columns that are displayed when you view a DataFrame. The display.max_columns option specifies the maximum number of columns that will be displayed when you view a DataFrame. For example, if you wanted to view all of the columns in a DataFrame you could use the following code:

```
pd.set_option('display.max_columns', None)
```

##### Using Pandas display.max_rows
Similar to the display.max_columns option, the display.max_rows option specifies the maximum number of rows that will be displayed when you view a DataFrame. For example, if you wanted to view all of the rows in a DataFrame you could use the following code:

```
pd.set_option('display.max_rows', None)
```

##### Using Pandas display.width
The display.width option specifies the maximum width of the output display. By default, the maximum width is 80 characters. However, you can increase this value if you want to view more columns in the output. For example, if you wanted to view all of the columns in a DataFrame you could use the following code:

```
pd.set_option('display.width', None)
```
