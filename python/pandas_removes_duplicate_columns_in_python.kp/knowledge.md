---
title: How to eliminate duplicate columns in Python pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To remove duplicate columns in pandas, you can use the drop\_duplicates() function with the argument axis=1.
---

**Contents**

[TOC]

## Identify Duplicate Columns

The first step is to identify the duplicate columns in a Pandas DataFrame. We can accomplish this by looping through the columns and comparing each one to the others.

```
duplicates = []
for i, col in enumerate(df.columns):
    for j in range(i+1, len(df.columns)):
        if df[col].equals(df[df.columns[j]]):
            duplicates.append(df.columns[j])
```

Here, we create an empty list called duplicates and loop through the columns in the DataFrame. For each column, we loop through the remaining columns (i+1) and compare it to the other columns by using the equals() method. If they are equal, we add the column name to our duplicates list.

## Remove Duplicate Columns

Once we have identified the duplicate columns, we can remove them from the DataFrame using the drop() method.

```
df = df.drop(duplicates, axis=1)
```

Here, we call the drop() method on our DataFrame (df) and pass in our duplicates list as the columns to drop. The axis=1 parameter tells Pandas to drop columns instead of rows.

## Keep One Copy of Duplicate Columns

If we want to keep one copy of the duplicate columns instead of removing them all, we can modify our code slightly.

```
duplicates = []
for i, col in enumerate(df.columns):
    for j in range(i+1, len(df.columns)):
        if df[col].equals(df[df.columns[j]]):
            duplicates.append(j)

df = df.drop(df.columns[duplicates], axis=1)
```

Instead of appending the name of the duplicate column to our list, we append its index. Then, when we call drop(), we pass in the columns parameter as df.columns[duplicates]. This will drop all of the duplicate columns except for the first one.

## Conclusion

Identifying and removing duplicate columns in a Pandas DataFrame is a simple process once you know how to do it. By using the equals() method to compare columns and the drop() method to remove them, we can ensure that our data is clean and accurate.
