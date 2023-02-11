---
title: Transform a pandas dataframe into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The Pandas DataFrame can be converted to JSON format by using the DataFrame.to\_json() method.
---

**Contents**

[TOC]

#### Section 1: Initial Setup

Before converting a Pandas DataFrame to JSON format, it is important to make sure that the DataFrame is in the correct format. This may include ensuring that all columns have the correct data types, any missing values have been filled in, and all data has been normalized.

#### Section 2: Convert DataFrame to JSON

Once the DataFrame is in the correct format, the `.to_json()` method can be used to convert it to JSON format. This method takes an argument of `orient` which specifies the type of JSON output. The options are `'split'`, `'records'`, `'index'`, and `'columns'`, and the default is `'columns'`.

#### Section 3: Output JSON

The `.to_json()` method returns a string of the JSON output. To write the JSON to a file, the `.write_json()` method can be used, which takes a file path as an argument.

#### Section 4: Read JSON

To read the JSON back into a DataFrame, the `.read_json()` method can be used. This method takes the file path as an argument, and returns the DataFrame.
