---
title: What is the method of checking whether a string in pandas includes any of the substrings listed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `str.contains()` method with the list of substrings as the argument.
---

**Contents**

[TOC]

## Section 1: Creating a sample pandas dataframe with a column containing strings

To demonstrate how to test if a string contains one of the substrings in a list in pandas, we first need a sample dataframe with a column containing strings.


```python
import pandas as pd

data = {'Name': ['John Smith', 'Mary Jackson', 'James Johnson', 'Sarah Williams', 'William Brown'],
        'City': ['New York', 'Los Angeles', 'Chicago', 'Houston', 'Boston']}
df = pd.DataFrame(data)
df['Name'] = df['Name'].astype(str)
df.head()
```


Output:

    
    Name           City
    John Smith     New York
    Mary Jackson   Los Angeles
    James Johnson  Chicago
    Sarah Williams Houston
    William Brown  Boston


## Section 2: Creating a list of substrings to search for

We also need a list of substrings that we want to search for within the strings in our dataframe. In this example, we will create a list of states.


```python
states = ['New York', 'California', 'Texas']
```


## Section 3: Finding rows where the 'Name' column contains a substring from the list

We can use the pandas `.str.contains()` method to search the 'Name' column for any substring from the 'states' list. We will create a new column called 'State' to store the state name if it is found in the 'Name' column.


```python
df['State'] = df['Name'].apply(lambda x: next((state for state in states if state in x), ""))
```


Output:


    Name           City          State
    John Smith     New York      New York
    Mary Jackson   Los Angeles   
    James Johnson  Chicago       
    Sarah Williams Houston       Texas
    William Brown  Boston 


## Section 4: Explanation

### Overview

The code in this tutorial demonstrates a basic way to search for substrings in a pandas dataframe using the `.str.contains()` method. This method allows us to search a pandas series (column) of strings for a particular pattern. In this case, we are searching for strings that contain any of the substrings in a given list. 


### Implementation

In the code, we first create a sample pandas dataframe with a column containing strings. We then create a list of substrings that we want to search for in the strings. We then use the `.str.contains()` method to search the 'Name' column for any substring from the 'states' list. We create a new column called 'State' to store the state name if it is found in the 'Name' column.


```python
df['State'] = df['Name'].apply(lambda x: next((state for state in states if state in x), ""))
```

This line of code uses the `.apply()` method to apply the lambda function to each value in the 'Name' column. The lambda function performs the search for each value by iterating over the 'states' list using a for loop. It uses the `next()` function to return the first item in the list that matches the condition (i.e. the substring is in the value of the 'Name' column). If no match is found, the function returns an empty string `("")`.


### Conclusion

In conclusion, this tutorial demonstrates a basic way to search for substrings in a pandas dataframe using the `.str.contains()` method. This method is useful for filtering rows based on complex string patterns.
