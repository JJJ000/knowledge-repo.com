---
title: Received a JSON string that caused a jsondecodeerror due to an expected comma delimiter
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: No valid JSON can contain an unescaped comma.
---

**Contents**

[TOC]

### Section 1: Overview
JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging data between a server and a web application. It is a text-based data format that is easy for humans to read and write, and easy for machines to parse and generate.

### Section 2: JSONDecodeError
JSONDecodeError is an error that occurs when a JSON string is not properly formatted. This error occurs when a comma (“,”) is missing from a JSON string, or when there is an extra comma in the string.

### Section 3: Example
For example, the following JSON string is missing a comma after the "name" field:

```
{
  "name": "John Smith"
  "age": 30
}
```

This will result in a JSONDecodeError, as the string is not properly formatted.

### Section 4: Solution
The solution is to ensure that all JSON strings are properly formatted, with commas separating each field. The following is a properly formatted JSON string:

```
{
  "name": "John Smith",
  "age": 30
}
```
