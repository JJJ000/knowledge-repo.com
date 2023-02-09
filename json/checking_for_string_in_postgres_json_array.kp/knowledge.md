---
title: See if a particular string is present in a Postgres JSON array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, you can use the `@>` operator to check if a JSON array contains a string in Postgres.
---

**Contents**

[TOC]

**Section 1: Overview**

Postgres JSON arrays are a type of data structure that can store multiple elements of various data types, including strings. It is possible to check if a Postgres JSON array contains a string using the `@>` operator.

**Section 2: Syntax**

The syntax for checking if a Postgres JSON array contains a string is as follows:

`json_array_column_name @> 'string_value'`

Where `json_array_column_name` is the name of the JSON array column and `string_value` is the string value you are checking for.

**Section 3: Example**

For example, if we had a table called `users` with a column called `hobbies` that stored a JSON array of strings, we could check if the `hobbies` column contained the string `"reading"` like this:

`SELECT * FROM users WHERE hobbies @> '"reading"';`

**Section 4: Output**

This query would return all rows from the `users` table where the `hobbies` column contained the string `"reading"`.
