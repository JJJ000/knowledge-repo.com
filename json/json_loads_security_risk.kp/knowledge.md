---
title: Can json.loads() be used to execute arbitrary code?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: No, json.loads() is not vulnerable to arbitrary code execution.
---

**Contents**

[TOC]

1. What is json.loads()?

json.loads() is a function in Python's json module that deserializes a string of JSON data into a Python object. It takes a string as an argument and returns a Python object such as a dictionary or list.

2. Is json.loads() Vulnerable to Arbitrary Code Execution?

No, json.loads() is not vulnerable to arbitrary code execution. It is designed to only parse valid JSON strings and will not execute any code. It is not possible to inject code into the JSON string and have it execute.
