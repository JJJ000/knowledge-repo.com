---
title: What is the syntax for querying a JSON column for objects with no values?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the WHERE clause to check if the JSON column is an empty object (i.e. `{}`).
---

**Contents**

[TOC]

1. Overview
2. Syntax
3. Examples
4. Additional Resources

## Overview
JSON columns are a great way to store and manipulate data. Many databases support JSON columns, and they are becoming increasingly popular. However, when querying a JSON column, it can be difficult to identify empty objects. Fortunately, there are some techniques that can be used to query a JSON column for empty objects. 

## Syntax
The syntax for querying a JSON column for empty objects will vary depending on the database system being used. Generally, the syntax will involve the use of a JSON function to check if the object is empty. For example, in PostgreSQL, the syntax would be: 

```
SELECT * FROM table WHERE JSON_OBJECT_LENGTH(column_name) = 0;
```

## Examples
Here is an example of how to query a JSON column for empty objects in PostgreSQL:

```
SELECT * FROM table WHERE JSON_OBJECT_LENGTH(column_name) = 0;
```

This query will return all rows from the table where the JSON column is empty. 

## Additional Resources
For more information on querying a JSON column for empty objects, please see the following resources: 

- [PostgreSQL JSON Documentation](https://www.postgresql.org/docs/current/functions-json.html)
- [MySQL JSON Documentation](https://dev.mysql.com/doc/refman/8.0/en/json-functions.html)
- [SQL Server JSON Documentation](https://docs.microsoft.com/en-us/sql/t-sql/functions/json-functions-transact-sql?view=sql-server-ver15)
