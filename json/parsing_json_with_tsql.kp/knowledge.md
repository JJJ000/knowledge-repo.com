---
title: Analyze JSON data using tsql
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: It is possible to parse JSON in TSQL using the built-in OPENJSON function.
---

**Contents**

[TOC]

**Section 1: Introduction**

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is a text-based, human-readable format that is easy to parse and generate. JSON has become increasingly popular in recent years, and is now widely used in web applications, databases, and other applications. In TSQL, JSON can be used to store and manipulate data in a structured way.

**Section 2: Parsing JSON in TSQL**

Parsing JSON in TSQL is relatively straightforward. TSQL supports a number of built-in functions that can be used to parse and manipulate JSON data. The most commonly used functions are JSON_VALUE, JSON_QUERY, and OPENJSON.

JSON_VALUE is used to extract a scalar value from a JSON string. It takes a JSON string and an expression as parameters and returns the value of the expression in the JSON string.

JSON_QUERY is used to extract an object or an array from a JSON string. It takes a JSON string and an expression as parameters and returns the value of the expression in the JSON string.

OPENJSON is used to parse an array of JSON objects. It takes a JSON string and a set of columns as parameters and returns a table with the specified columns and the values of the JSON string.

**Section 3: Example**

To illustrate how to parse JSON in TSQL, let's consider an example. We have the following JSON string:

```
{
  "name": "John Doe",
  "age": 34,
  "address": {
    "street": "123 Main Street",
    "city": "New York",
    "state": "NY"
  }
}
```

We can use the JSON_VALUE function to extract the value of the "name" property:

```
SELECT JSON_VALUE(@json, '$.name') AS Name
```

This will return the following result:

| Name      |
|-----------|
| John Doe  |

We can also use JSON_QUERY to extract the address object:

```
SELECT JSON_QUERY(@json, '$.address') AS Address
```

This will return the following result:

| Address                                             |
|---------------------------------------------------|
| {"street":"123 Main Street","city":"New York","state":"NY"} |

Finally, we can use OPENJSON to parse the address object into columns:

```
SELECT * FROM OPENJSON(JSON_QUERY(@json, '$.address'))
WITH (
  Street VARCHAR(100),
  City VARCHAR(100),
  State VARCHAR(2)
)
```

This will return the following result:

| Street    | City      | State |
|-----------|-----------|-------|
| 123 Main Street | New York | NY   |

**Section 4: Conclusion**

In conclusion, parsing JSON in TSQL is relatively straightforward. TSQL supports a number of built-in functions that can be used to parse and manipulate JSON data. By using these functions, we can easily extract scalar values, objects, and arrays from JSON strings, and parse them into columns.
