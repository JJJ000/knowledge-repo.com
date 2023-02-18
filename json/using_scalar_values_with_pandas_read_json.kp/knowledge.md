---
title: If you are only using scalar values, you must supply an index when using the pandas read_json command
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The index must be provided if all values in the JSON file are scalar values.
---

**Contents**

[TOC]

## What Does This Mean?
This error message is encountered when attempting to use the `read_json` function in pandas. It means that when all of the values in the JSON data being read are scalar values, such as strings, numbers, and booleans, the user must specify an index. 

## What is an Index?
An index is a way of labeling the data in a pandas DataFrame. It is used to identify each row in the DataFrame. Generally, an index can be either a single column or multiple columns. 

## Why Is an Index Necessary?
When all of the values in the JSON data being read are scalar values, an index is necessary in order to distinguish between the different rows. Without an index, the data will be read in as a single row of data, which will make it difficult to analyze. 

## How to Specify an Index
The index can be specified when using the `read_json` function by passing the argument `index` to the function. This argument should be set to the name of the column or columns that should be used as the index.
