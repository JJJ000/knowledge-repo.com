---
title: Are quotes required for the JSON keys?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, JSON keys must be surrounded by double quotes.
---

**Contents**

[TOC]

#### Yes

JSON keys must be surrounded by double quotes in order to be valid. This is because JSON is a subset of the JavaScript language and in JavaScript, object keys must be surrounded by double quotes.

#### Example

For example, the following JSON is valid because the keys are surrounded by double quotes:

```json
{
  "name": "John Doe",
  "age": 25
}
```

#### No

However, some JSON parsers may allow keys to be unquoted if they follow the same rules as JavaScript identifiers. This means they must start with a letter, underscore, or dollar sign and can contain alphanumeric characters, underscores, and dollar signs.

#### Example

For example, the following JSON is valid because the keys follow the same rules as JavaScript identifiers:

```json
{
  name: "John Doe",
  age: 25
}
```
