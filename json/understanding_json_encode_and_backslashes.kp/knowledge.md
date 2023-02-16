---
title: What is the purpose of json_encode adding backslashes?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: json\_encode adds backslashes to escape certain characters, such as quotation marks, to ensure the string is valid JSON.
---

**Contents**

[TOC]

## What is JSON?
JSON (JavaScript Object Notation) is an open standard file format that is used for exchanging data between applications. It is a lightweight data-interchange format that is easy for humans to read and write, and for machines to parse and generate.

## What is json_encode?
json_encode is a PHP function that is used to convert a PHP value to a JSON string. It takes a PHP value and returns a JSON-encoded string representation of it.

## Why is json_encode Adding Backslashes?
json_encode adds backslashes to characters that have a special meaning in JSON. This is done to prevent the characters from being interpreted as part of the JSON string. For example, a double quote (") is escaped with a backslash (\") so that it is not interpreted as the end of the string. Similarly, a single quote (') is escaped with a backslash (\') so that it is not interpreted as the end of the string.
