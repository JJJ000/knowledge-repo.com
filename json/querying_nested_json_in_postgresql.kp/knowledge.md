---
title: Querying nested JSON in postgresql
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: PostgreSQL supports querying JSON data using the JSONPath language, which allows for nested JSON queries.
---

**Contents**

[TOC]

**Section 1: Overview**

PostgreSQL is a powerful, open-source object-relational database system. It supports a wide range of data types, including the JSON data type, which allows for the storage and retrieval of complex, nested JSON documents. This makes it possible to query nested JSON data using the powerful PostgreSQL query language.

**Section 2: JSON Data Structure**

JSON data is structured as a set of key-value pairs. Each key-value pair is composed of a key (which is a string) and a value (which can be a string, number, boolean, array, or object). An array is a collection of values, and an object is a collection of key-value pairs. Nested JSON documents are composed of multiple levels of nested objects and arrays.

**Section 3: Querying Nested JSON**

PostgreSQL provides a number of functions and operators that can be used to query nested JSON documents. The most commonly used functions are the `jsonb_array_elements()` and `jsonb_object_keys()` functions, which allow for the extraction of values from nested JSON documents. Additionally, the `->` and `->>` operators can be used to query specific keys in nested JSON documents.

**Section 4: Examples**

For example, the following query can be used to extract all the values from a nested JSON document:

```sql
SELECT jsonb_array_elements(data)
FROM table;
```

The following query can be used to extract the value of a specific key in a nested JSON document:

```sql
SELECT data->'key'
FROM table;
```

Finally, the following query can be used to extract the value of a specific key in a nested JSON document as a text value:

```sql
SELECT data->>'key'
FROM table;
```
