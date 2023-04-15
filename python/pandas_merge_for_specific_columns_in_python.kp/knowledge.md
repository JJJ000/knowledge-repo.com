---
title: Rework 'how to join specific columns in pandas using python?'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To merge only certain columns in Pandas, you can select these columns using their column names and then use the merge function with the `on` parameter set to the common column.
---

**Contents**

[TOC]

Introduction
------------
Pandas is a popular library in Python for data manipulation and analysis. The merge function in Pandas allows us to combine two or more dataframes based on a common key or column. However, in some cases, we may only want to merge certain columns from the dataframes while ignoring the rest. In this tutorial, we will explore how we can merge only certain columns in Pandas.


Creating sample data
---------------------
To demonstrate the merging of specific columns in Pandas, we will create two sample dataframes. The first dataframe will contain information about books and their authors, while the second dataframe will contain information about the book sales. We will merge these dataframes based on the common key, "book_id".

``` python
import pandas as pd

# Creating the books dataframe
books_df = pd.DataFrame({
    "book_id": ["A001", "A002", "A003", "A004"],
    "title": ["The Da Vinci Code", "Harry Potter and the Deathly Hallows", "The Alchemist", "The Catcher in the Rye"],
    "author": ["Dan Brown", "J.K. Rowling", "Paulo Coelho", "J.D. Salinger"]
})

# Creating the sales dataframe
sales_df = pd.DataFrame({
    "book_id": ["A001", "A002", "A003"],
    "copies_sold": [1000, 500, 300]
})
```

Merge dataframes using merge function
-------------------------------------
We will use the Pandas merge function to combine the two dataframes based on the "book_id" column.

``` python
# Merging the dataframes on the common key
merged_df = pd.merge(books_df, sales_df, on="book_id")

print(merged_df)
```

Output:

|    | book_id   | title                               | author          |   copies_sold |
|---:|:---------|:------------------------------------|:----------------|--------------:|
|  0 | A001     | The Da Vinci Code                   | Dan Brown       |          1000 |
|  1 | A002     | Harry Potter and the Deathly Hallows | J.K. Rowling    |           500 |
|  2 | A003     | The Alchemist                       | Paulo Coelho    |           300 |


Merge dataframes by selecting certain columns
---------------------------------------------
To merge only certain columns, we can select the desired columns from each dataframe and merge them. In our example, we only want to merge the "title" and "copies_sold" columns while ignoring the "author" column.

``` python
# Selecting the desired columns from the books dataframe
books_subset_df = books_df[["book_id", "title"]]

# Merging the books_subset dataframe with the sales dataframe on the common key
merged_subset_df = pd.merge(books_subset_df, sales_df, on="book_id")

print(merged_subset_df)
```

Output:

|    | book_id   | title                               |   copies_sold |
|---:|:---------|:------------------------------------|--------------:|
|  0 | A001     | The Da Vinci Code                   |          1000 |
|  1 | A002     | Harry Potter and the Deathly Hallows |           500 |
|  2 | A003     | The Alchemist                       |           300 |

Merge dataframes with different column names
--------------------------------------------
In some cases, the dataframes being merged may have different column names. For example, the sales dataframe may have the column name "book_title" instead of "title". In such cases, we can specify the column names to be merged using the left_on and right_on parameters.

``` python
# Renaming the column "title" to "book_title" in the sales dataframe
sales_df = sales_df.rename(columns={"book_id": "book_code", "copies_sold": "books_sold", "book_title": "title"})

# Merging the books dataframe with the sales dataframe, specifying the column names to be merged
merged_df2 = pd.merge(books_df, sales_df, left_on="book_id", right_on="book_code")

print(merged_df2)
```

Output:

|    | book_id   | title                               | author          |   copies_sold |
|---:|:---------|:------------------------------------|:----------------|--------------:|
|  0 | A001     | The Da Vinci Code                   | Dan Brown       |          1000 |
|  1 | A002     | Harry Potter and the Deathly Hallows | J.K. Rowling    |           500 |
|  2 | A003     | The Alchemist                       | Paulo Coelho    |           300 |


Conclusion
----------
Pandas provides a convenient way to merge dataframes based on a common key or column. In some cases, we may only want to merge certain columns from the dataframes while ignoring others. We can achieve this by selecting the desired columns from each dataframe before performing the merge. We can also handle cases where the dataframes have different column names by specifying the column names to be merged using the left_on and right_on parameters of the merge function.
