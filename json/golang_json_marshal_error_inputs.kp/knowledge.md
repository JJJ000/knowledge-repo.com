---
title: Under what circumstances will golang's json.marshal return an error?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Passing a Go type that cannot be represented as a valid JSON value, such as a function, will cause json.Marshal to return an error.
---

**Contents**

[TOC]

1. Invalid Type:
Any type that is not supported by the json package, such as functions or channels, will cause `json.Marshal` to return an error. 

2. Cyclic Structures:
If a structure contains a cyclic reference, `json.Marshal` will return an error.

3. Unsupported Values:
Values that are not supported by the json package, such as `Infinity` or `NaN`, will cause `json.Marshal` to return an error.

4. Invalid Characters:
If a string contains invalid characters, such as a control character, `json.Marshal` will return an error.
