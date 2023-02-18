---
title: What is the syntax for searching for a specific string in a JSON Postgres data type column?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: You can use the JSONB\_EXISTS function to search for a specific string in a JSON Postgres data type column.
---

**Contents**

[TOC]

## Section 1: Create an Index

The first step to searching for a specific string in a Postgres JSON data type column is to create an index. This will enable Postgres to quickly find the data you are looking for. To create an index, you can use the `CREATE INDEX` command. For example, if you have a table called `my_table` with a column called `my_json_column`, you can create an index on that column as follows:

```
CREATE INDEX my_json_column_idx ON my_table USING GIN (my_json_column);
```

## Section 2: Use the JSONB_PATH_EXISTS Function

Once the index is created, you can use the `JSONB_PATH_EXISTS` function to search for a specific string in the JSON data type column. This function takes two parameters: the name of the column and the path of the key-value pair you are looking for. For example, if you are searching for the value `"foo"` in the key-value pair `"bar": "foo"`, the query would look like this:

```
SELECT * 
FROM my_table 
WHERE JSONB_PATH_EXISTS(my_json_column, '$.bar') AND my_json_column->>'bar' = 'foo';
```

## Section 3: Use the JSONB_EXISTS Function

If you are searching for a specific string in an array within the JSON data type column, you can use the `JSONB_EXISTS` function. This function takes three parameters: the name of the column, the path of the array, and the value you are searching for. For example, if you are searching for the value `"foo"` in the array `["bar", "foo", "baz"]`, the query would look like this:

```
SELECT * 
FROM my_table 
WHERE JSONB_EXISTS(my_json_column, '$.arr[*]', 'foo');
```

## Section 4: Use Wildcards

If you are searching for a string that may contain wildcards, you can use the `LIKE` operator. For example, if you are searching for any string that starts with `"foo"`, the query would look like this:

```
SELECT * 
FROM my_table 
WHERE my_json_column->>'bar' LIKE 'foo%';
```
