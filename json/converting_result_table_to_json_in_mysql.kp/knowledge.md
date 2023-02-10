---
title: What is the syntax for converting a result table to a JSON array in mysql?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON\_ARRAYAGG() function to convert a result table to a JSON array in MySQL.
---

**Contents**

[TOC]

## Section 1: Retrieving the Data

In order to convert the result table to a JSON array in MySQL, the data must first be retrieved. This can be done by using the `SELECT` statement to retrieve the desired columns and rows from the database.

## Section 2: Using the JSON_ARRAYAGG Function

Once the data has been retrieved, the `JSON_ARRAYAGG` function can be used to convert the result table into a JSON array. This function takes in a column name and will return a JSON array containing the values from that column.

## Section 3: Combining Multiple Columns

If multiple columns need to be included in the JSON array, the `CONCAT` function can be used to combine multiple columns into a single column. This combined column can then be used as the argument for the `JSON_ARRAYAGG` function.

## Section 4: Outputting the Result

The final step is to output the result of the query. This can be done by using the `SELECT` statement with the `JSON_ARRAYAGG` function as the argument. The resulting JSON array can then be outputted to the console or stored in a variable for further processing.
