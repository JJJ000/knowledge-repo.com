---
title: Pandas parse nested json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Pandas can read nested JSON using the `json\_normalize` function.
---

**Contents**

[TOC]

# Section 1: Overview
Pandas is a powerful library for data analysis and manipulation. It provides a wide range of tools and functions for working with structured and unstructured data. One of the most useful features of Pandas is its ability to read and write data in a variety of formats, including nested JSON.

# Section 2: Parsing Nested JSON
When parsing nested JSON with Pandas, the read_json() function can be used to read the data into a Pandas DataFrame. The function takes a path or URL to the JSON file as its first argument and a list of fields to extract from the JSON as its second argument. The fields can be nested and the read_json() function will automatically parse the nested data into columns.

# Section 3: Manipulating Nested JSON
Once the nested JSON has been parsed into a DataFrame, it can be manipulated in the same way as any other DataFrame. This includes sorting, filtering, and aggregating data, as well as performing mathematical operations.

# Section 4: Writing Nested JSON
Pandas also provides the ability to write nested JSON. The to_json() function can be used to write the data back to a JSON file. The function takes a path or URL to the JSON file as its first argument and a list of fields to include in the JSON as its second argument. The fields can be nested and the to_json() function will automatically create the appropriate nested structure for the JSON.
