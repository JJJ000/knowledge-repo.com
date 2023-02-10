---
title: Python json.loads returns items prefixed with 'u'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, json.loads does not return items prefixing with `u`.
---

**Contents**

[TOC]

## What is json.loads?

`json.loads` is a built-in Python method that is used to convert a JSON string into a Python object. It takes a JSON string as an argument and returns a Python object.

## What Does json.loads Return?

When `json.loads` is used, it will return a Python object, such as a dictionary, list, or string. This object will contain all of the data that was in the original JSON string.

## Does json.loads Return Items Prefixing with 'u'?

No, `json.loads` does not return items prefixing with 'u'. The 'u' is actually a prefix that is added to strings when they are encoded as unicode. This is done to ensure that any special characters are properly encoded and can be read correctly.
