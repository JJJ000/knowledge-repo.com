---
title: Rewording boolean indexing in pandas with logical operators
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The logical operators for Boolean indexing in Pandas in Python are `&` for `and`, `|` for `or`, and `~` for `not`.
---

**Contents**

[TOC]

Introduction 

Boolean indexing is a powerful feature in Pandas, allowing us to select subsets of data based on conditions. We can use logical operators to create more complex conditions and filter data more precisely.

In this article, we’ll explore the logical operators commonly used for Boolean indexing in Pandas and see some examples.

AND operator 

The AND operator is denoted by the ampersand (&) symbol in Pandas. This operator is used to combine two or more conditions, and only the rows that satisfy all the conditions will be selected.

Example: 

Suppose we want to select all rows where the ‘age’ column is greater than 30 and the ‘gender’ column is ‘male’. We can use the following code:

```python
df[(df['age'] > 30) & (df['gender'] == 'male')]
```

OR operator 

The OR operator is denoted by the pipe (|) symbol in Pandas. This operator is used to combine two or more conditions, and the rows that satisfy at least one of the conditions will be selected.

Example: 

Suppose we want to select all rows where the ‘age’ column is greater than 30 or the ‘gender’ column is ‘female’. We can use the following code:

```python
df[(df['age'] > 30) | (df['gender'] == 'female')]
```

NOT operator 

The NOT operator is denoted by the tilde (~) symbol in Pandas. This operator is used to negate a condition, and the rows that do not satisfy the condition will be selected.

Example: 

Suppose we want to select all rows where the ‘age’ column is not greater than 30. We can use the following code:

```python
df[~(df['age'] > 30)]
```

Combining multiple conditions 

We can combine multiple conditions using logical operators to create more complex conditions.

Example: 

Suppose we want to select all rows where the ‘age’ column is between 30 and 40 and the ‘gender’ column is ‘male’. We can use the following code:

```python
df[(df['age'] >= 30) & (df['age'] <= 40) & (df['gender'] == 'male')]
```

Conclusion 

Boolean indexing with Pandas is a powerful feature that allows us to select data based on conditions. We can use logical operators to create more complex conditions and filter data more precisely. In this article, we saw the commonly used logical operators for Boolean indexing in Pandas, and some examples for their usage.
