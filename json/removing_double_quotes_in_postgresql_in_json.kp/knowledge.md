---
title: Eliminate quotation marks from the output of a function in postgresql
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the function REPLACE() to replace double quotes with an empty string.
---

**Contents**

[TOC]

**Section 1: Overview**

PostgreSQL is an open-source relational database management system that supports a wide variety of data types, including JSON. When a function returns a JSON data type, it will often include double quotes around the values. Removing these double quotes can be done using various methods, depending on the specific use case.

**Section 2: Using String Functions**

One way to remove double quotes from a returned JSON value is to use the built-in string functions in PostgreSQL. The REPLACE() function can be used to replace double quotes with an empty string, which will effectively remove them from the output. For example, the following statement would remove double quotes from a JSON string: 

`SELECT REPLACE(json_string, '"', '')`

**Section 3: Using JSON Functions**

Another way to remove double quotes from a returned JSON value is to use the built-in JSON functions in PostgreSQL. The JSON_UNQUOTE() function can be used to remove double quotes from a JSON string. For example, the following statement would remove double quotes from a JSON string:

`SELECT JSON_UNQUOTE(json_string)`

**Section 4: Using Custom Functions**

If neither of the two methods above are suitable for the use case, it is also possible to create a custom function in PostgreSQL to remove double quotes from a JSON string. This can be done using the PL/pgSQL language, which allows for the creation of custom functions that can be used to manipulate data. For example, the following code could be used to create a custom function to remove double quotes from a JSON string:

`CREATE OR REPLACE FUNCTION remove_double_quotes(json_string text) RETURNS text AS $$
  DECLARE
    result text;
  BEGIN
    result := REPLACE(json_string, '"', '');
    RETURN result;
  END;
$$ LANGUAGE plpgsql;`
