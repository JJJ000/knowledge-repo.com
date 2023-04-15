---
title: What is the method to convert true/false values to 1/0 in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the astype() method to convert the Boolean column to an integer column with 1s and 0s.
---

**Contents**

[TOC]

# Section 1: Creating a sample DataFrame

# Let us create a sample DataFrame that contains True/False values
import pandas as pd
df = pd.DataFrame({'A': [True, False, True], 'B': [False, True, False]})
print(df)

# Output:
#        A      B
# 0   True  False
# 1  False   True
# 2   True  False


# Section 2: Using the map function

# We can use the map function to convert True/False values to 1/0.
# Define a dictionary to map True to 1 and False to 0, and then apply the map function to the DataFrame.
df = df.applymap({True: 1, False: 0}.get)
print(df)

# Output:
#    A  B
# 0  1  0
# 1  0  1
# 2  1  0


# Section 3: Using the astype function

# Another way to convert True/False to 1/0 is to use the astype function to convert the boolean values to integer values.
df = df.astype(int)
print(df)

# Output:
#    A  B
# 0  1  0
# 1  0  1
# 2  1  0


# Section 4: Using the replace function

# We can also use the replace function to convert True/False to 1/0.
# Define a dictionary to replace True with 1 and False with 0, and then apply the replace function to the DataFrame.
df = df.replace({True: 1, False: 0})
print(df)

# Output:
#    A  B
# 0  1  0
# 1  0  1
# 2  1  0
