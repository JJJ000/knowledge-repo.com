---
title: Construct a pandas dataframe by adding one row at a time
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: One can create a Pandas Dataframe by appending a dictionary or a list of values to the Dataframe one row at a time using the Dataframe.append() method.
---

**Contents**

[TOC]

### Section 1: Import Libraries

§ Code

import pandas as pd
 
§ Markdown

### Section 2: Create a Dataframe

§ Code

# Create an empty dataframe
df = pd.DataFrame()
 
§ Markdown

### Section 3: Append Rows

§ Code

# Create a dictionary with the data
data = {'Name':['John', 'Bob', 'Sue', 'Steve'],
        'Age':[30, 40, 20, 35]}

# Append the row
df = df.append(data, ignore_index=True)
 
§ Markdown

### Section 4: View the Dataframe

§ Code

# View the dataframe
df

§ Output

> ['   Name  Age\n', '0  John   30\n', '1   Bob   40\n', '2   Sue   20\n', '3  Steve   35']

 
§ END OF DOC
