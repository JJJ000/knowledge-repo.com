---
title: Change the data type of a pandas column containing missing values to "int"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `fillna()` method to fill the NaNs with a suitable integer, then use the `astype()` method to convert the column to `int` type.
---

**Contents**

[TOC]

#### Section 1: Converting the Data Type

The data type of a Pandas column containing NaNs can be converted to `int` using the `.astype()` method. This method takes a single argument, which specifies the data type to be converted to.

For example, the following code will convert the data type of a Pandas column to `int`:

```python
df['column_name'] = df['column_name'].astype(int)
```

#### Section 2: Handling NaNs

When converting a Pandas column containing NaNs to `int`, the NaNs must be handled. This can be done by specifying the `errors` parameter of the `.astype()` method. The `errors` parameter takes a string value which specifies how to handle the NaNs.

For example, the following code will convert the data type of a Pandas column to `int` while ignoring any NaNs:

```python
df['column_name'] = df['column_name'].astype(int, errors='ignore')
```

#### Section 3: Replacing NaNs

Alternatively, the NaNs can be replaced with a specified value. This can be done using the `.fillna()` method. This method takes a single argument which specifies the value to be used to replace the NaNs.

For example, the following code will convert the data type of a Pandas column to `int` while replacing any NaNs with the value 0:

```python
df['column_name'] = df['column_name'].fillna(0).astype(int)
```

#### Section 4: Error Handling

It is important to note that if the data type conversion fails, an error will be raised. This can be handled using a `try`/`except` block.

For example, the following code will convert the data type of a Pandas column to `int` while handling any errors that may be raised:

```python
try:
    df['column_name'] = df['column_name'].astype(int)
except ValueError:
    df['column_name'] = df['column_name'].fillna(0).astype(int)
```
