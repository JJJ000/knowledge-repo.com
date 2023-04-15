---
title: How to use json.dumps to save utf-8 texts as utf-8, instead of as a `\u` escape sequence
authors:
- cool_wizard
tags:
- json
- python
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: json.dumps can be used with the ensure_ascii parameter set to False to save UTF-8 texts as UTF-8, not as a `\u` escape sequence.
---

**Contents**

[TOC]

### What is json.dumps?

json.dumps is a Python method used to serialize an object into a JSON string. It takes an object as an argument and returns a JSON-encoded string.

### What is UTF-8?

UTF-8 is a character encoding standard that uses 8-bit units to represent all possible characters. It is the most widely used character encoding system and is the default encoding for HTML, XML, and most other modern programming languages.

### How to Save UTF-8 Texts with json.dumps?

When using json.dumps to save UTF-8 texts, you must specify the encoding parameter as ‘utf-8’. This will ensure that the strings are encoded as UTF-8 and not as a `\u` escape sequence.

### What is a `\u` Escape Sequence?

A `\u` escape sequence is a Unicode character that is encoded as a 4-byte sequence of hexadecimal numbers. It is used to represent characters that cannot be represented in the ASCII character set.
