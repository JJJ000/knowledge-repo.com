---
title: What is the best way to retrieve all keys from a JSON column in postgres?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the `jsonb\_object\_keys()` function to get all keys from a JSON column in Postgres as a JSON array.
---

**Contents**

[TOC]

**Section 1: Retrieving Keys from a JSON Column**

The Postgres JSON data type allows you to store and query data in a JSON format. To retrieve the keys from a JSON column, you can use the `jsonb_object_keys()` function. This function will return an array of all the keys in the specified JSON column.

**Section 2: Using the jsonb_object_keys() Function**

The `jsonb_object_keys()` function requires a single parameter, which is the name of the JSON column. For example, if the name of the JSON column is `json_data`, the query would look like this:

```
SELECT jsonb_object_keys(json_data)
FROM my_table;
```

This will return an array of all the keys in the `json_data` column.

**Section 3: Example Usage**

Let's say we have a table called `my_table` with a JSON column called `json_data`. The `json_data` column contains the following JSON object:

```
{
  "name": "John Doe",
  "age": 30,
  "address": "123 Main Street"
}
```

We can use the `jsonb_object_keys()` function to get the keys from this JSON object:

```
SELECT jsonb_object_keys(json_data)
FROM my_table;
```

This will return the following array:

```
["name", "age", "address"]
```

**Section 4: Conclusion**

The `jsonb_object_keys()` function is a useful tool for retrieving the keys from a JSON column in Postgres. It is simple to use and can be used to quickly get the keys from a JSON object.
