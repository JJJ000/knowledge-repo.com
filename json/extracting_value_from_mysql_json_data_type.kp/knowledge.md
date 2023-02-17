---
title: Retrieve value from MySQL JSON data type without quotation marks
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the JSON\_EXTRACT() function to extract values from a JSON column without quotation marks.
---

**Contents**

[TOC]

# Section 1: Using MySQL JSON_EXTRACT()
The MySQL JSON_EXTRACT() function can be used to extract a value from a JSON string without quotation marks. The syntax of the function is:

`JSON_EXTRACT(json_doc, path[, path]...)`

Where `json_doc` is the JSON document and `path` is the path to the value to be extracted.

# Section 2: Example
For example, to extract the value `123` from the following JSON document:

`{"foo": "bar", "baz": 123}`

The following query can be used:

`SELECT JSON_EXTRACT(doc, '$.baz') FROM my_table;`

# Section 3: Limitations
The JSON_EXTRACT() function is limited to extracting values from a single level of the JSON document. It cannot be used to extract values from nested objects or arrays.

# Section 4: Alternatives
If the JSON document contains nested objects or arrays, then the MySQL JSON_UNQUOTE() function can be used to extract the value without quotation marks. The syntax of the function is:

`JSON_UNQUOTE(json_value)`

Where `json_value` is the JSON value to be unquoted.
