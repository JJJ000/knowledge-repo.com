---
title: Can JSON contain strings that span multiple lines?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, multi-line strings are allowed in JSON, as long as they are enclosed in double-quotes.
---

**Contents**

[TOC]

### Syntax

Multi-line strings in JSON are represented using the backslash (\\) character followed by a newline character. This allows for strings that span multiple lines and contain line breaks.

### Example

The following is an example of a multi-line string in JSON:

```json
{
  "name": "John Doe",
  "address": "123 Main Street\\
  Anytown, USA"
}
```

### Limitations

The only limitation of multi-line strings in JSON is that they cannot contain unescaped line breaks. This means that any line breaks must be preceded by a backslash (\\).
