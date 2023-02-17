---
title: Retrieving nested JSON data from sql server using openjson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, SQL Server OPENJSON can read nested json.
---

**Contents**

[TOC]

1. Introduction
2. Overview of OPENJSON
3. Reading Nested JSON with OPENJSON
4. Conclusion

### Introduction

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is a text-based format that is easy for humans to read and write and also easy for machines to parse and generate. JSON is widely used for data interchange between web applications and web services. It is often used to store data in a structured format and to transfer data between web applications and web services.

SQL Server provides a built-in function called OPENJSON that can be used to read JSON data and store it in a relational format. This function can be used to read both simple and nested JSON data.

### Overview of OPENJSON

OPENJSON is a built-in function in SQL Server that can be used to read JSON data and store it in a relational format. It takes a JSON string as an input and returns a set of rows that represent the data in the JSON string. The OPENJSON function can be used to read both simple and nested JSON data.

The function takes a JSON string as an input and returns a set of rows that represent the data in the JSON string. The OPENJSON function can be used to read both simple and nested JSON data.

### Reading Nested JSON with OPENJSON

Nested JSON data can be read using the OPENJSON function in SQL Server. The OPENJSON function takes a JSON string as an input and returns a set of rows that represent the data in the JSON string.

The OPENJSON function can be used to read nested JSON data by specifying a path to the nested data in the JSON string. The path is specified using the ‘$’ operator followed by the name of the nested property.

For example, the following query reads the ‘name’ property from a nested JSON object:

SELECT value FROM OPENJSON('{"name": "John Doe"}', '$.name')

This query returns the value ‘John Doe’ from the nested JSON object.

### Conclusion

The SQL Server OPENJSON function can be used to read both simple and nested JSON data. The function takes a JSON string as an input and returns a set of rows that represent the data in the JSON string. The OPENJSON function can be used to read nested JSON data by specifying a path to the nested data in the JSON string.
