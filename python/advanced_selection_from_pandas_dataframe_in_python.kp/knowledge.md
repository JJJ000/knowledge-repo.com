---
title: Filtering a pandas.dataframe using intricate conditions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the .query() method to select rows from a DataFrame based on a given set of criteria.
---

**Contents**

[TOC]

**Section 1: Creating the Criteria**

The first step in selecting with complex criteria from a pandas.DataFrame is to create the criteria. This can be done by setting up a list of conditions that must be met for a row to be included in the selection. For example, if we wanted to select all rows in a DataFrame where the value in the “Name” column is “John” and the value in the “Age” column is greater than 25, we could create the following list of conditions:

- Name == 'John'
- Age > 25

**Section 2: Using the Criteria**

Once the criteria has been created, it can be used to select the desired rows from the DataFrame. This can be done by using the pandas.DataFrame.query() method, which allows us to pass in the criteria as a string. For example, if we wanted to select all rows in a DataFrame where the value in the “Name” column is “John” and the value in the “Age” column is greater than 25, we could use the following code:

```
df.query('Name == "John" & Age > 25')
```

**Section 3: Combining Criteria**

If multiple criteria need to be combined, the pandas.DataFrame.query() method can be used to do so. For example, if we wanted to select all rows in a DataFrame where the value in the “Name” column is “John” and the value in the “Age” column is greater than 25, but also where the value in the “Gender” column is “Male”, we could use the following code:

```
df.query('Name == "John" & Age > 25 & Gender == "Male"')
```

**Section 4: Using Multiple Criteria**

The pandas.DataFrame.query() method also allows for multiple criteria to be used in a single query. For example, if we wanted to select all rows in a DataFrame where the value in the “Name” column is “John” and the value in the “Age” column is greater than 25, but also where the value in the “Gender” column is “Male” or “Female”, we could use the following code:

```
df.query('Name == "John" & Age > 25 & (Gender == "Male" | Gender == "Female")')
```
