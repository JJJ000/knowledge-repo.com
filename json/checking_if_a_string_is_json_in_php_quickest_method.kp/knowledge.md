---
title: What is the quickest method to determine if a string is a valid JSON in php?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json\_decode() function to check if a string is valid JSON.
---

**Contents**

[TOC]

1. **Using json_decode()**
The fastest way to check if a string is JSON in PHP is to use the `json_decode()` function. This function takes a JSON string as its parameter and returns the corresponding PHP value. If the string is valid JSON, the function will return an object or array representation of the JSON data. If the string is not valid JSON, the function will return `NULL`.

2. **Using json_last_error()**
After using `json_decode()`, you can use the `json_last_error()` function to check if the JSON string was valid. This function returns an integer value that indicates the type of error that occurred. If the string was valid JSON, the function will return `JSON_ERROR_NONE`.

3. **Using json_last_error_msg()**
If you want more detailed information about the error, you can use the `json_last_error_msg()` function. This function returns a string that describes the error that occurred.

4. **Using Regular Expressions**
You can also use regular expressions to check if a string is valid JSON. This approach is not recommended, however, as it is much slower than using the built-in functions.
