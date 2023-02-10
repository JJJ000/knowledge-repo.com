---
title: Converting numbers to strings using php's json_encode function
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: PHP`s json\_encode function encodes all values as strings by default.
---

**Contents**

[TOC]

# Section 1: What is PHP json_encode?
PHP json_encode is a PHP function that converts a PHP value into a JSON string. It is used to encode data in JSON format for transmission over a network connection.

# Section 2: How Does json_encode Encode Numbers?
By default, json_encode will encode numbers as strings. This means that any numbers that are passed to it will be converted to a string representation. For example, a number such as `123` will be converted to `"123"`.

# Section 3: Why Does json_encode Encode Numbers as Strings?
json_encode encodes numbers as strings for compatibility reasons. This ensures that the data is compatible with other applications and systems that may be expecting strings instead of numbers.

# Section 4: How to Avoid Encoding Numbers as Strings
If you need to avoid encoding numbers as strings, you can use the `JSON_NUMERIC_CHECK` flag when calling json_encode. This will ensure that numbers are encoded as numbers instead of strings.
