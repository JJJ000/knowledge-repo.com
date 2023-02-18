---
title: Is it necessary to put quotation marks around JSON numbers?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: No, JSON numbers must not be quoted.
---

**Contents**

[TOC]

### Yes 

JSON numbers can be quoted in JSON. This is especially useful when the number contains a decimal point, as JSON does not support decimal points in unquoted numbers. Additionally, quoting a number can make it easier to read, as it can make it easier to distinguish a number from a string. 

### Syntax

When quoting a number in JSON, the number should be surrounded by double quotes. For example, the number `5` would be written as `"5"`. 

### Examples

Below are some examples of quoting numbers in JSON. 

```
{
    "num1": "5",
    "num2": "3.14"
}
```

```
{
    "total": "100.00"
}
```
