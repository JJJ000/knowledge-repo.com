---
title: What is the syntax for querying fields within the postgresql JSON datatype?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can query using fields inside the PostgreSQL JSON datatype by using the JSON operators -> and ->>.
---

**Contents**

[TOC]

**Section 1: Overview**

PostgreSQL's JSON datatype allows for the storage of JSON documents in a database. This provides a powerful way to query and manipulate JSON data stored in the database. This guide will provide an overview of how to query using fields inside the JSON datatype in PostgreSQL.

**Section 2: Creating a Table with a JSON Column**

The first step in querying with the JSON datatype is to create a table with a JSON column. To do this, use the CREATE TABLE statement and specify the JSON datatype for the column. For example:

```
CREATE TABLE my_table (
  id serial PRIMARY KEY,
  data json
);
```

**Section 3: Inserting Data into the Table**

Once the table has been created, data can be inserted into the JSON column using the INSERT statement. For example:

```
INSERT INTO my_table (data) VALUES ('{"name": "John Doe", "age": 42}');
```

**Section 4: Querying the Table**

Finally, to query the table using fields inside the JSON datatype, use the JSON_EXTRACT_PATH_TEXT function. For example, to query for all records where the name field is equal to "John Doe":

```
SELECT * FROM my_table WHERE JSON_EXTRACT_PATH_TEXT(data, 'name') = 'John Doe';
```
