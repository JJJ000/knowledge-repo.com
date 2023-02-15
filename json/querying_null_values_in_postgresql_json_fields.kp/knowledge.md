---
title: What is the syntax for querying null values in a JSON field type in postgresql?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the IS NULL operator in a WHERE clause to query for null values in a JSON field type in PostgreSQL.
---

**Contents**

[TOC]

### Using IS NULL

The most straightforward way to query for null values in a JSON field type in PostgreSQL is to use the `IS NULL` operator. This can be used to check if a specific field is null, or if any field in the JSON is null.

For example, to check if the `name` field of a JSON field is null, the following query would be used:

```sql
SELECT * FROM table WHERE json_field->'name' IS NULL
```

To check if any field in the JSON is null, the following query would be used:

```sql
SELECT * FROM table WHERE json_field ? 'null'
```

### Using JSON_EACH

Another way to query for null values in a JSON field type in PostgreSQL is to use the `JSON_EACH` function. This function allows you to iterate through each key-value pair in the JSON and check for null values.

For example, the following query would be used to check if any field in the JSON is null:

```sql
SELECT * FROM table WHERE JSON_EACH(json_field) IS NULL
```

### Using JSON_ARRAY_LENGTH

Another way to query for null values in a JSON field type in PostgreSQL is to use the `JSON_ARRAY_LENGTH` function. This function allows you to check the length of an array in the JSON, and if the length is 0, then it can be assumed that the array is null.

For example, the following query would be used to check if the `name` field of a JSON field is null:

```sql
SELECT * FROM table WHERE JSON_ARRAY_LENGTH(json_field->'name') = 0
```
