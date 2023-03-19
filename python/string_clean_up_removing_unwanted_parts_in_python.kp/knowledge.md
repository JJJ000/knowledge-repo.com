---
title: Eliminate irrelevant sections from the strings in a specific column
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can use the string method split combined with list comprehension to remove unwanted parts from strings in a column in Python.
---

**Contents**

[TOC]

## Introduction
Sometimes we need to clean up the data in our datasets by removing unwanted parts from strings in a column. This can be achieved using different string manipulation techniques in Python. In this article, we will discuss some of the most commonly used techniques for removing unwanted parts from strings in a column.

## Using the split() method
The split() method is a Python string manipulation method that splits a string into a list of substrings based on a delimiter. We can use this method to remove unwanted parts of a string by splitting it and then rejoining the desired parts.

For example, suppose we have a column with strings that contain a date and time in the format 'YYYY-MM-DD-HH-MM-SS'. We want to remove the time component of the string. We can achieve this as follows:

``` python
# Importing pandas library 
import pandas as pd

# Creating a sample dataframe 
data = {'dateandtime': ['2022-10-05-12-30-45', '2022-10-04-11-20-25', '2022-10-03-09-10-05']}
df = pd.DataFrame(data)

# Split the string using "-" delimiter and use only the first three parts
df['date_only'] = df.dateandtime.apply(lambda x: '-'.join(x.split('-')[:3]))

# Output
print(df)
```

Output:

|    | dateandtime         | date_only   |
|---:|:--------------------|:------------|
|  0 | 2022-10-05-12-30-45 | 2022-10-05  |
|  1 | 2022-10-04-11-20-25 | 2022-10-04  |
|  2 | 2022-10-03-09-10-05 | 2022-10-03  |

In the above code snippet, we create a new column 'date_only' in the dataframe 'df' by applying the split() method on the 'dateandtime' column to create a list of substrings, which are then joined using the join() method to create the desired output.

## Using the replace() method
The replace() method is another useful string manipulation method in Python that replaces the occurrences of a substring in a string with a new substring.

Suppose we have a column with strings that contain multiple spaces between words. We want to remove these extra spaces and keep only one space between words. We can achieve this using the replace() method as follows:

``` python
# Creating a sample dataframe
data = {'text': ['This   is     a      sentence.', 'So  is     this      one.']}
df = pd.DataFrame(data)

# Removing extra spaces using replace() method
df['clean_text'] = df.text.str.replace(' +', ' ', regex=True)

# Output
print(df)
```

Output:

|    | text                          | clean_text                   |
|---:|:------------------------------|:-----------------------------|
|  0 | This   is     a      sentence.| This is a sentence.          |
|  1 | So  is     this      one.     | So is this one.              |

In the above code snippet, we create a new column 'clean_text' in the dataframe 'df' by applying the replace() method on the 'text' column. We replace all the occurrences of multiple spaces with a single space using a regular expression pattern ' +' that matches one or more spaces.

## Using the split() method with the str accessor
We can also use the split() method with the str accessor provided by Pandas to remove unwanted parts of strings in a column. The str accessor provides a convenient way to apply string manipulation methods on all the elements of a column.

Suppose we have a column with strings that contain email addresses. We want to remove the domain name from the email addresses. We can achieve this using the split() method with the str accessor as follows:

``` python
# Creating a sample dataframe
data = {'email': ['john.doe@example.com', 'jane.doe@example.com']}
df = pd.DataFrame(data)

# Removing the domain name using split() method with str accessor
df['username'] = df.email.str.split('@').str[0]

# Output
print(df)
```

Output:

|    | email                 | username |
|---:|:---------------------|:---------|
|  0 | john.doe@example.com | john.doe |
|  1 | jane.doe@example.com | jane.doe |

In the above code snippet, we create a new column 'username' in the dataframe 'df' by applying the split() method with the str accessor on the 'email' column to split the email addresses into a list of substrings and then use the indexing operator [0] to retain only the username part of the email address.

## Conclusion
In this article, we discussed three commonly used techniques for removing unwanted parts from strings in a column in Python. These techniques are using the split() method, using the replace() method, and using the split() method with the str accessor. Depending on the structure and complexity of the data, we can choose one of these techniques or a combination of them to achieve the desired data cleaning.
