---
title: How to quickly expand multiple list columns in a pandas dataframe
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use list comprehension to iterate through the columns, unnest each column, and store the values in a new JSON object.
---

**Contents**

[TOC]

**Section 1: Overview**

Unnesting (or exploding) multiple list columns in a pandas DataFrame in JSON is a common task that can be accomplished in a few different ways. This article will provide an overview of two of the most efficient methods for performing this task: using the json_normalize function and using the apply function. Both of these methods will be explained in detail in the subsequent sections.

**Section 2: json_normalize**

The json_normalize function is a built-in pandas function that can be used to convert a list of dictionaries or a list of lists into a tabular format. This function can be used to efficiently flatten multiple list columns in a DataFrame into a single column of values. To use the json_normalize function, you need to provide the DataFrame and the list columns that you want to flatten as parameters. The json_normalize function will then return a new DataFrame with the flattened list columns as individual columns. 

**Section 3: apply**

The apply function is another built-in pandas function that can be used to efficiently flatten multiple list columns in a DataFrame. To use the apply function, you need to provide the DataFrame and the list columns that you want to flatten as parameters. The apply function will then loop through each row in the DataFrame and apply a function to each row. The function can be used to flatten the list columns in the row and return a new DataFrame with the flattened list columns as individual columns. 

**Section 4: Conclusion**

Unnesting multiple list columns in a pandas DataFrame in JSON can be done efficiently using either the json_normalize function or the apply function. Both of these methods will provide a new DataFrame with the flattened list columns as individual columns. Depending on the size and complexity of the DataFrame, one of these methods may be more efficient than the other.
