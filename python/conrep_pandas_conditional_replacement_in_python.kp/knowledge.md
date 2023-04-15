---
title: Rewording pandas replacement on a condition basis
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The conditional replace function in pandas allows you to replace specific values in a DataFrame based on a condition.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is a popular library for data manipulation and analysis in Python. One of its main features is the ability to replace values in a DataFrame using the replace() method. However, it is often necessary to conditionally replace values based on certain criteria, such as replacing all values above a certain threshold or replacing values in a specific column. In this article, we will explore different methods for conditionally replacing values in Pandas.

Section 2: Using Boolean Indexing for Conditional Replacement
Boolean indexing is a powerful feature in Pandas that allows us to filter data based on a condition. We can use boolean indexing for conditional replacement by first creating a boolean mask that identifies the positions of the values that meet the condition, and then using the mask to replace the values.

For example, let's say we have a DataFrame called df with a column called 'score'. We want to replace all values above 80 with the value 100. We can do this using boolean indexing as follows:

```
mask = df['score'] > 80
df.loc[mask, 'score'] = 100
```

This creates a boolean mask that identifies all the rows where the value in the 'score' column is greater than 80. We then use the .loc[] method to select only those rows and set the value in the 'score' column to 100.

Section 3: Using the replace() Method with a Dictionary
Another method for conditionally replacing values in Pandas is to use the replace() method with a dictionary that maps the old values to the new values based on a condition.

Let's say we have a DataFrame called df with a column called 'gender' that contains the values 'male' and 'female'. We want to replace all occurrences of 'male' with 'M' and all occurrences of 'female' with 'F'. We can do this using the replace() method with a dictionary as follows:

```
mapping = {'male': 'M', 'female': 'F'}
df['gender'] = df['gender'].replace(mapping)
```

This creates a dictionary that maps 'male' to 'M' and 'female' to 'F'. We then use the replace() method to replace all occurrences of the old values with the new values.

Section 4: Using the apply() Method with a Function
Finally, we can also conditionally replace values using the apply() method with a function that maps the old values to the new values based on a condition. This method is useful when the condition is more complex and cannot be easily expressed as a boolean mask or a dictionary.

For example, let's say we have a DataFrame called df with a column called 'age'. We want to replace all values above 50 with the value 50, and all values below 18 with the value 18. We can do this using the apply() method with a function as follows:

```
def replace_age(age):
    if age > 50:
        return 50
    elif age < 18:
        return 18
    else:
        return age

df['age'] = df['age'].apply(replace_age)
```

This defines a function called replace_age that maps the old values to the new values based on the condition. We then use the apply() method to apply this function to each value in the 'age' column of the DataFrame.
