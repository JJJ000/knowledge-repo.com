---
title: Modify a value in pandas based on another value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the .loc method to select rows and columns based on certain conditions, then assign a new value to the selected cells.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is one of the most popular data processing libraries for Python. It offers powerful data structures that make it easy to work with datasets of all shapes and sizes. One common task when working with data is updating values based on the values of other columns. In this tutorial, we will learn how to change one value based on another value in pandas.

Section 2: Data Preparation
To demonstrate how to update values based on other values in pandas, we need some data. In this tutorial, we will use the sales data of a store. Below is a sample code snippet to create a pandas DataFrame for the sales data.

```python
import pandas as pd

data = {'Name': ['Tom', 'Jack', 'Steve', 'Ricky'], 
        'Product': ['TV', 'Laptop', 'Table', 'Chair'],
        'Sale Price': [1500, 1250, 50, 20],
        'Discount': [0.1, 0.2, 0.3, 0.4]}

df = pd.DataFrame(data)
print(df)
```
Output:
```
    Name Product  Sale Price  Discount
0    Tom      TV        1500       0.1
1   Jack  Laptop        1250       0.2
2  Steve   Table          50       0.3
3  Ricky   Chair          20       0.4
```

The DataFrame consists of four columns: Name, Product, Sale Price, and Discount. 

Section 3: Updating Values Based on Another Column
Suppose we want to update the Sale Price column by applying the discount on each product. To achieve this, we can use the apply() method in combination with a lambda function. Here’s how to do it:

```python
df['Sale Price'] = df.apply(lambda row: row['Sale Price'] - (row['Sale Price'] * row['Discount']), axis=1)
print(df)
```
Output:
```
    Name Product  Sale Price  Discount
0    Tom      TV      1350.0       0.1
1   Jack  Laptop      1000.0       0.2
2  Steve   Table        35.0       0.3
3  Ricky   Chair        12.0       0.4
```

As you can see, the Sale Price column now contains the new prices after applying the discount.

Section 4: Conclusion
In this tutorial, we learned how to update values based on another value in pandas. Specifically, we used the apply() method in combination with a lambda function to update the Sale Price column based on the Discount column. This is just one example of how powerful pandas can be when it comes to data processing. With pandas, you can quickly and easily process datasets of all shapes and sizes to extract valuable insights.
