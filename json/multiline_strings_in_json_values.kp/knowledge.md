---
title: Is it possible for a JSON value to contain a string that spans multiple lines?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, a JSON value can contain a multiline string as long as it is enclosed in double quotes.
---

**Contents**

[TOC]

## Yes
JSON values can contain multiline strings, as long as the strings are properly escaped.

## Escaping
When a string contains a newline character, the character must be escaped in order for the string to be valid JSON. This is done by adding a backslash (\) before the newline. For example, the following string contains two lines:

```
"This is a
multiline string"
```

In order to make this a valid JSON string, the newline character must be escaped like so:

```
"This is a\
multiline string"
```

## Usage
Multiline strings can be used in JSON objects, arrays, and even as the root value of a JSON document. For example, the following is a valid JSON document:

```
{
    "message": "This is a\
multiline string"
}
```

## Limitations
It is important to note that while multiline strings are supported in JSON, they are not supported in all JSON parsers. Some parsers may not recognize escaped newlines and could result in errors. It is important to check the documentation of the parser being used to ensure that it supports multiline strings.
