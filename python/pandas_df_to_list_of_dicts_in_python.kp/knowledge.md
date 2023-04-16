---
title: Converting a pandas dataframe into a list of dictionaries
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Convert the Pandas DataFrame to a list of dictionaries by using the DataFrame`s to\_dict() method.
---

**Contents**

[TOC]

## Section 1: Overview
Pandas DataFrame to List of Dictionaries is the process of converting a Pandas DataFrame into a list of dictionaries. This can be done by iterating over the rows of the DataFrame and creating a dictionary for each row. Each dictionary in the list will contain the column names and their associated values for that row. 

## Section 2: Steps
1. Create a DataFrame. 
2. Iterate over the rows of the DataFrame. 
3. Create a dictionary for each row. 
4. Add the column names and their associated values for that row to the dictionary. 
5. Append the dictionary to a list. 

## Section 3: Example

For example, let's say we have a DataFrame with three columns and three rows: 

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
|    A     |    B     |    C     |
|    D     |    E     |    F     |
|    G     |    H     |    I     |

The resulting list of dictionaries would be: 

[{'Column 1': 'A', 'Column 2': 'B', 'Column 3': 'C'}, 
{'Column 1': 'D', 'Column 2': 'E', 'Column 3': 'F'}, 
{'Column 1': 'G', 'Column 2': 'H', 'Column 3': 'I'}]

## Section 4: Conclusion
By following the steps outlined above, it is possible to convert a Pandas DataFrame into a list of dictionaries. This can be a useful way to store and manipulate data in Python.
