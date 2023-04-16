---
title: What is the process for adding an empty column to a dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DataFrame.assign() method to add an empty column to a dataframe in Python.
---

**Contents**

[TOC]

## 1. Import Libraries

The first step is to import the necessary libraries. For this task, we will need to import the Pandas library:

```python
import pandas as pd
```

## 2. Create Dataframe

The next step is to create the dataframe. Here, we will create a simple dataframe with three columns and two rows:

```python
data = {'Name': ['John', 'Jane'], 
        'Age': [20, 21], 
        'Country': ['USA', 'Canada']
       } 

df = pd.DataFrame(data) 
```

## 3. Add Empty Column

Now, we can add an empty column to the dataframe by using the `insert()` method. This method takes two arguments: the index of the column to be inserted and the name of the column. In this case, we will insert the empty column at index 3, and we will name it 'Gender':

```python
df.insert(3, 'Gender', '')
```

## 4. Print Dataframe

Finally, we can print the dataframe to see the result:

```python
print(df)
```

The output should look like this:

| Name | Age | Country | Gender |
|------|-----|---------|--------|
| John | 20  | USA     |        |
| Jane | 21  | Canada  |        |
