---
title: How can I convert float values to integers in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the Pandas astype() method to convert floats to ints in Pandas.
---

**Contents**

[TOC]

#### Option 1: Using the astype() Method

This method can be used to convert floats to ints in Pandas. The syntax for this is: 

`df['column_name'] = df['column_name'].astype(int)`

For example, to convert the 'price' column from the following DataFrame to ints: 

```
   item  price
0  ball   5.99
1  bat    8.99
2  glove  4.99
```

We would use the following code: 

`df['price'] = df['price'].astype(int)`

#### Option 2: Using the to_numeric() Method

This method can also be used to convert floats to ints in Pandas. The syntax for this is: 

`pd.to_numeric(df['column_name'], downcast='integer')`

For example, to convert the 'price' column from the following DataFrame to ints: 

```
   item  price
0  ball   5.99
1  bat    8.99
2  glove  4.99
```

We would use the following code: 

`pd.to_numeric(df['price'], downcast='integer')`
