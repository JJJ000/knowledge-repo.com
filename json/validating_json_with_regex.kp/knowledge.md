---
title: Regular expression to check if a string is a valid json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The JSON must match the regular expression `^\s*(\{.*\}|\[.*\])\s*$` to be valid.
---

**Contents**

[TOC]

### Section 1: Using Regular Expressions

Regular expressions can be used to validate JSON strings. The following regex can be used to validate a JSON string:

```
^\s*\{\s*(("(\\.|[^"\\\n\r])*?"|[^,{}\s][^\n\r]*)\s*\:\s*(("(\\.|[^"\\\n\r])*?"|[^,\[\]\s][^\n\r]*|\[[\s\S]*?\])\s*(,\s*(("(\\.|[^"\\\n\r])*?"|[^,{}\s][^\n\r]*)\s*\:\s*(("(\\.|[^"\\\n\r])*?"|[^,\[\]\s][^\n\r]*|\[[\s\S]*?\])\s*)*)?\})\s*$
```

### Section 2: Using Parsers

Another way to validate JSON strings is to use a parser. Parsers can be used to parse the JSON string and check for any syntax errors. If the parser finds any syntax errors, then the JSON string is not valid.

### Section 3: Using JSON Schema

JSON Schema is a standard for validating JSON documents. It defines a schema that can be used to validate JSON strings. If a JSON string does not match the schema, then it is not valid.

### Section 4: Using Libraries

There are many libraries available for validating JSON strings. These libraries can be used to validate JSON strings against a set of rules. They can also be used to validate JSON strings against a JSON Schema.
