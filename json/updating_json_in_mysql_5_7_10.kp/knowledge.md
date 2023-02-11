---
title: What is the process for changing a JSON data type column in MySQL 5.7.10?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the JSON\_SET() function to update a JSON data type column in MySQL 5.7.10.
---

**Contents**

[TOC]

1. **Creating a Table with a JSON Column**

To create a table with a JSON data type column, you need to use the `JSON` data type when creating the table.

For example, to create a table called `test_table` with a JSON data type column called `data`:

```sql
CREATE TABLE test_table (
  id INT NOT NULL AUTO_INCREMENT,
  data JSON,
  PRIMARY KEY (id)
);
```

2. **Inserting Data into a JSON Column**

To insert data into a JSON column, you need to use the `JSON_SET` function.

For example, to insert a JSON object into the `data` column of the `test_table` table:

```sql
INSERT INTO test_table (data)
  VALUES (JSON_SET('{}', '$.name', 'John'));
```

3. **Updating Data in a JSON Column**

To update data in a JSON column, you need to use the `JSON_SET` function.

For example, to update the `name` field in the `data` column of the `test_table` table:

```sql
UPDATE test_table
  SET data = JSON_SET(data, '$.name', 'Jane')
  WHERE id = 1;
```

4. **Deleting Data from a JSON Column**

To delete data from a JSON column, you need to use the `JSON_REMOVE` function.

For example, to delete the `name` field from the `data` column of the `test_table` table:

```sql
UPDATE test_table
  SET data = JSON_REMOVE(data, '$.name')
  WHERE id = 1;
```
