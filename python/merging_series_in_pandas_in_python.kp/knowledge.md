---
title: Creating a dataframe from two series objects in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can combine two Series into a DataFrame in pandas by using the DataFrame constructor and passing in the two Series as arguments.
---

**Contents**

[TOC]

#### Section 1: Creating the Series

To combine two Series into a DataFrame in pandas, we must first create the Series. This can be done by creating two separate Series and assigning them to variables. 

For example: 

```
s1 = pd.Series([1, 2, 3, 4])
s2 = pd.Series([5, 6, 7, 8])
```

#### Section 2: Creating the DataFrame

Next, we create the DataFrame by passing the two Series as arguments to the `pd.DataFrame()` function. 

For example: 

```
df = pd.DataFrame(data=[s1, s2])
```

#### Section 3: Viewing the DataFrame

We can now view the DataFrame by printing it. 

For example: 

```
print(df)
```

This will output the following: 

```
   0  1  2  3
0  1  2  3  4
1  5  6  7  8
```

#### Section 4: Renaming the Columns

Finally, we can rename the columns of the DataFrame by passing the `columns` argument to the `pd.DataFrame()` function. 

For example: 

```
df = pd.DataFrame(data=[s1, s2], columns=['A', 'B', 'C', 'D'])
```

This will output the following: 

```
   A  B  C  D
0  1  2  3  4
1  5  6  7  8
```
