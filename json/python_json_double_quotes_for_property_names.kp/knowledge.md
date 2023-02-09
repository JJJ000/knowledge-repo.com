---
title: Expect the name of a property to be enclosed in quotation marks when using Python and json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, property names must be enclosed in double quotes when using JSON.
---

**Contents**

[TOC]

# Introduction

JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging data between different applications. It is based on a subset of the JavaScript programming language and is commonly used for data serialization and transmission. In JSON, property names must be enclosed in double quotes.

# Why Property Names Must be Enclosed in Double Quotes

Property names in JSON must be enclosed in double quotes to ensure that they are treated as strings. This is important because some programming languages, such as JavaScript, treat unquoted property names as variables. Without the double quotes, the property name could be misinterpreted as a variable and lead to unexpected results.

# Examples

In the following example, the property name "name" must be enclosed in double quotes to ensure that it is treated as a string: 

```
{
  "name": "John Doe"
}
```

Similarly, in the following example, the property name "age" must be enclosed in double quotes to ensure that it is treated as a string: 

```
{
  "age": 25
}
```

# Conclusion

In conclusion, property names in JSON must be enclosed in double quotes to ensure that they are treated as strings. This is important to prevent unexpected results due to misinterpretation of the property name as a variable.
