---
title: Decode JSON containing both familiar and unfamiliar field names
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the `json.Unmarshal` function to decode JSON data into a struct, allowing you to access known field names and ignore unknown field names.
---

**Contents**

[TOC]

**Section 1: Retrieving Known Fields**

When unmarshaling JSON with known field names, the process is relatively straightforward. The JSON data can be easily unmarshalled into a struct, where each field of the struct corresponds to a field in the JSON data. The struct should be populated with the appropriate data types, and the JSON data can then be unmarshalled into the struct using the json.Unmarshal function.

**Section 2: Retrieving Unknown Fields**

When unmarshalling JSON with unknown field names, the process is slightly more complicated. One approach is to use a map[string]interface{} type to store the data. This type allows for arbitrary key-value pairs to be stored, and the JSON data can be unmarshalled into the map using the json.Unmarshal function. Once the data is stored in the map, the values can then be accessed and manipulated.

**Section 3: Error Handling**

When unmarshalling JSON, it is important to handle any errors that may occur. The json.Unmarshal function returns an error if the data cannot be unmarshalled. This error should be checked, and appropriate action should be taken if an error is encountered.

**Section 4: Performance Considerations**

When unmarshalling JSON, it is important to consider the performance implications of the process. Unmarshalling large amounts of data can be computationally expensive, and it is important to optimize the process for the best performance. This can be done by using efficient data structures and algorithms, as well as by avoiding unnecessary operations.
