---
title: Filter the rows of a dataframe using chained operators in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Using operator chaining, rows of a DataFrame can be filtered by passing multiple conditions in the form of boolean expressions to the DataFrame`s `.loc` accessor.
---

**Contents**

[TOC]

### Section 1: Overview
Pandas is a powerful Python library for data analysis. It provides a set of methods to filter rows of a DataFrame using operator chaining. Operator chaining is a technique that allows you to apply multiple operations to a DataFrame in a single line of code. This can be useful for quickly filtering out unwanted rows from a DataFrame.

### Section 2: Syntax
The syntax for using operator chaining to filter a DataFrame is as follows:

`df.query('<condition1> & <condition2> & <condition3>')`

Where `df` is the DataFrame, and `<condition1>`, `<condition2>`, and `<condition3>` are conditions that must be satisfied in order for a row to be included in the resulting DataFrame.

### Section 3: Example
As an example, consider the following DataFrame:

| Name | Age | Gender |
|------|-----|--------|
| Bob  | 25  | Male   |
| Jane | 21  | Female |
| John | 30  | Male   |

To filter this DataFrame to only include rows where the age is greater than 25 and the gender is male, we can use the following code:

`df.query('Age > 25 & Gender == "Male"')`

This will return the following DataFrame:

| Name | Age | Gender |
|------|-----|--------|
| John | 30  | Male   |

### Section 4: Conclusion
In conclusion, operator chaining is a powerful technique for quickly filtering rows of a DataFrame in Pandas. It allows you to apply multiple conditions to a DataFrame in a single line of code, making it a useful tool for data analysis.
