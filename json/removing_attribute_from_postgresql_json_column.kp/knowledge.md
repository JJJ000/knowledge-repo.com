---
title: Delete an attribute from a JSON column in postgresql
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the jsonb\_set() function to remove an attribute from a JSON column.
---

**Contents**

[TOC]

#### Section 1: Overview
PostgreSQL provides an array of functions to manipulate JSON data. One of the functions is the `jsonb_set()` function, which allows a user to remove an attribute from a JSON column in PostgreSQL.

#### Section 2: Syntax
The syntax for the `jsonb_set()` function is as follows:

`jsonb_set(target jsonb, path text[], new_value jsonb [, create_missing boolean])`

#### Section 3: Example
Let's say we have a table named `users` with a JSON column named `data`:

```
CREATE TABLE users (
  id serial PRIMARY KEY,
  data jsonb
);
```

We can use the `jsonb_set()` function to remove an attribute from the `data` column:

```
UPDATE users
SET data = jsonb_set(data, '{name}', NULL)
WHERE id = 1;
```

In this example, we are removing the `name` attribute from the `data` column of the row with `id` equal to `1`.

#### Section 4: Conclusion
The `jsonb_set()` function can be used to remove an attribute from a JSON column in PostgreSQL. This function can be used to update a single row or multiple rows in a table.
