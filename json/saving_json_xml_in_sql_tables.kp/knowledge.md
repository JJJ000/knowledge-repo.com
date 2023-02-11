---
title: How can I store JSON or xml data in an sql table?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can save JSON or XML data in an SQL Table by using the JSON or XML data type.
---

**Contents**

[TOC]

1. Prerequisites
------
Before saving JSON or XML data in an SQL Table, the table must be created with the appropriate data types. For example, if the JSON or XML data contains a string, the corresponding table column must be of the data type string.

2. Creating the Table
------
Once the table is created, the JSON or XML data can be saved in the table by using the INSERT statement. The INSERT statement requires the column names and the values to be inserted. The values must be in the correct format for the data type of the corresponding column.

3. Saving the Data
------
The INSERT statement can be used to save the JSON or XML data in the table. This can be done by using the appropriate functions for the data type of the column. For example, for a string data type column, the JSON_VALUE() or XML_VALUE() functions can be used to extract the value from the JSON or XML data and save it in the table.

4. Retrieving the Data
------
The data saved in the table can be retrieved by using the SELECT statement. The SELECT statement requires the column names and the values to be retrieved. The values returned by the SELECT statement will be in the correct format for the data type of the corresponding column.
