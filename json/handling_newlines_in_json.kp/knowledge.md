---
title: What is the best way to deal with line breaks in json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the \n escape sequence to represent newlines in JSON strings.
---

**Contents**

[TOC]

## 1. Escaping Newlines

Newlines can be escaped in JSON by using the `\n` escape sequence. This sequence will be interpreted as a newline when the JSON is parsed. For example, the following JSON string contains a newline character:

```
{
  "message": "Hello\nWorld"
}
```

## 2. Multiline Strings

In some cases, it may be more convenient to use a multiline string instead of escaping newlines. This can be done by wrapping a string in triple quotes (`"""`). For example:

```
{
  "message": """Hello
World"""
}
```

## 3. Raw Strings

In Python, raw strings can be used to represent strings with newlines. A raw string is prefixed with an `r` character. For example:

```
{
  "message": r"Hello\nWorld"
}
```

## 4. JSON Lines

JSON Lines is a format for storing multiple JSON objects in a single file. Each line in the file contains a single JSON object, and newlines are used to separate the objects. For example:

```
{"message": "Hello"}
{"message": "World"}
```
