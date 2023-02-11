---
title: Send information using the JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: JSON is a data format that is used to send and receive data in a structured format.
---

**Contents**

[TOC]

1. **Overview**
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write and for machines to parse and generate. It is based on a subset of the JavaScript Programming Language.

2. **Syntax**
JSON syntax is a subset of the JavaScript object notation syntax. Data is in name/value pairs. Data is separated by commas. Curly braces hold objects and each name is followed by ':' (colon), the name/value pairs are separated by , (comma). Square brackets hold arrays and values are separated by , (comma).

3. **POST Data in JSON Format**
POST data in JSON format is sent as a string in the body of an HTTP request. The data is encoded in the same way as query string parameters, but instead of being a list of unrelated values, it is a single JSON string. The Content-Type header of the request should be set to application/json.

4. **Example**
For example, if we wanted to send the following data in JSON format:

```
{
  "name": "John",
  "age": 30,
  "city": "New York"
}
```

We would send it as a string in the body of the request:

```
"{\"name\":\"John\",\"age\":30,\"city\":\"New York\"}"
```
