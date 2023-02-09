---
title: Is it possible to have duplicate keys within an object in JSON syntax?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, JSON syntax does not allow duplicate keys in an object.
---

**Contents**

[TOC]

No

## Reason

JSON syntax does not allow duplicate keys in an object. Each key in a JSON object must be unique and cannot be repeated. This is because JSON relies on key-value pairs to store data. If duplicate keys were allowed, the value associated with the key would be ambiguous and difficult to determine.

## Examples

For example, if a JSON object contained the following key-value pairs:

```json
{
  "name": "John Doe",
  "name": "Jane Doe"
}
```

It would be impossible to determine which name should be associated with the key "name".
