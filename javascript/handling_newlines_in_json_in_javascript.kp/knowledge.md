---
title: What is the best way to deal with line breaks in json?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the \n escape sequence to handle newlines in JSON in Javascript.
---

**Contents**

[TOC]

## Parsing JSON with Newlines

When parsing a JSON string that contains newlines, the most important thing to remember is that the newlines must be escaped. This can be done using the `JSON.parse()` method, which takes a string and returns a JavaScript object. The `JSON.parse()` method will automatically escape any newlines it finds in the string.

## Outputting JSON with Newlines

When outputting a JSON string with newlines, the `JSON.stringify()` method should be used. This method takes a JavaScript object and returns a string. The `JSON.stringify()` method will automatically escape any newlines it finds in the object.

## Escaping Newlines

If neither the `JSON.parse()` nor the `JSON.stringify()` methods are available, newlines can be escaped manually. This can be done by replacing any newlines with the `\n` character.

## Validating JSON

It is important to validate any JSON string that contains newlines before parsing or outputting it. This can be done using an online JSON validator or by using the `JSON.parse()` method and checking for any errors.
