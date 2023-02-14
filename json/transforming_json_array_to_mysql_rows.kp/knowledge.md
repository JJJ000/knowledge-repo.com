---
title: Transform a JSON array stored in MySQL into individual records
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: Use the JSON\_ARRAYAGG() function to convert a MySQL JSON array into a single JSON object.
---

**Contents**

[TOC]

Section 1: Use MySQL's JSON_EXTRACT() Function

MySQL provides the JSON_EXTRACT() function, which can be used to convert a JSON array into rows. This function takes in two parameters: the JSON array and the path to the desired element in the array. The function will then return the value of the element at the given path.

For example, if we have the following JSON array:

```
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 30
  }
]
```

We can use the JSON_EXTRACT() function to extract the name and age of each element in the array:

```
SELECT JSON_EXTRACT(data, '$.name') AS name, 
       JSON_EXTRACT(data, '$.age') AS age
FROM my_table
```

Section 2: Use MySQL's JSON_TABLE() Function

MySQL also provides the JSON_TABLE() function, which can be used to convert a JSON array into a table. This function takes in two parameters: the JSON array and the path to the desired element in the array. The function will then return the value of the element at the given path as a column in the table.

For example, if we have the following JSON array:

```
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 30
  }
]
```

We can use the JSON_TABLE() function to convert the array into a table with columns for the name and age of each element:

```
SELECT *
FROM JSON_TABLE(data, '$[*]'
  COLUMNS (
    name VARCHAR(100) PATH '$.name',
    age INTEGER PATH '$.age'
  )
) AS my_table
```

Section 3: Use MySQL's JSON_ARRAYAGG() Function

MySQL also provides the JSON_ARRAYAGG() function, which can be used to convert rows into a JSON array. This function takes in one parameter: the column containing the data to be converted into a JSON array. The function will then return a JSON array containing the values from the specified column.

For example, if we have the following table:

| name  | age |
|-------|-----|
| John  | 25  |
| Jane  | 30  |

We can use the JSON_ARRAYAGG() function to convert the table into a JSON array:

```
SELECT JSON_ARRAYAGG(name, age)
FROM my_table
```

This will return the following JSON array:

```
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 30
  }
]
```

Section 4: Use MySQL's JSON_OBJECTAGG() Function

MySQL also provides the JSON_OBJECTAGG() function, which can be used to convert rows into a JSON object. This function takes in two parameters: the column containing the data to be converted into a JSON object and the column containing the keys for the JSON object. The function will then return a JSON object containing the values from the specified columns.

For example, if we have the following table:

| name  | age |
|-------|-----|
| John  | 25  |
| Jane  | 30  |

We can use the JSON_OBJECTAGG() function to convert the table into a JSON object:

```
SELECT JSON_OBJECTAGG(name, age)
FROM my_table
```

This will return the following JSON object:

```
{
  "John": 25,
  "Jane": 30
}
```
