---
title: What would cause json_encode to produce an empty string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: It could return an empty string if the value passed to it is not a valid type for encoding.
---

**Contents**

[TOC]

# Causes
1. Invalid Data Type:
   If the data type of the value passed to json_encode is not supported, it will return an empty string.
2. Malformed Syntax:
   If the syntax of the code is incorrect, json_encode will return an empty string.

# Solutions
1. Check Data Types:
   Before passing a value to json_encode, check that it is a supported data type.
2. Debug Syntax:
   Check the syntax of the code to make sure it is correct.
