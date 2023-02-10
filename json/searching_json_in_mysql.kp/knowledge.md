---
title: What is the best way to query JSON data stored in a MySQL database?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON\_SEARCH() function to search JSON data in MySQL.
---

**Contents**

[TOC]

## Section 1: Create a JSON Column

In order to store JSON data in MySQL, you must first create a JSON column. This can be done by using the `JSON` data type when creating the table. 

For example, the following statement creates a table named `my_table` with a JSON column named `my_column`:

```sql
CREATE TABLE my_table (
    my_column JSON
);
```

## Section 2: Insert JSON Data

Once the JSON column is created, you can insert JSON data into it. This can be done by using the `INSERT` statement. 

For example, the following statement inserts a JSON document into the `my_column` column:

```sql
INSERT INTO my_table (my_column)
VALUES ('{
    "name": "John Doe",
    "age": 42
}');
```

## Section 3: Query JSON Data

Once the JSON data is inserted, you can query it using the `JSON_EXTRACT()` function. This function allows you to extract a single value from a JSON document. 

For example, the following statement returns the value of the `name` key from the JSON document:

```sql
SELECT JSON_EXTRACT(my_column, '$.name') 
FROM my_table;
```

## Section 4: Search JSON Data

You can also search JSON data using the `JSON_SEARCH()` function. This function allows you to search for a specific value within a JSON document. 

For example, the following statement returns the path of the `name` key from the JSON document:

```sql
SELECT JSON_SEARCH(my_column, 'one', 'John Doe') 
FROM my_table;
```
