---
title: Using Python json.loads, an error will be thrown if an invalid control character is encountered
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The json.loads function will raise a ValueError if any control characters are present in the string.
---

**Contents**

[TOC]

#### Section 1: Overview

The `json.loads()` function in Python is used to parse a JSON string and convert it into a Python object. It can be used to convert a JSON string into a dictionary, list, or other object. However, if the JSON string contains an invalid control character, `json.loads()` will raise a `JSONDecodeError`.

#### Section 2: Invalid Control Characters

An invalid control character is any character that is not allowed in a JSON string. This includes characters such as the backspace, form feed, and vertical tab. It also includes any non-printable characters such as the null character.

#### Section 3: Handling Invalid Control Characters

There are a few different ways to handle invalid control characters when using `json.loads()`. The first is to simply remove the invalid control character from the JSON string before passing it to `json.loads()`. This can be done by iterating over the string and removing any characters that are not allowed in a JSON string.

Another option is to use the `json.loads()` function's `strict` parameter. This parameter will cause `json.loads()` to raise a `JSONDecodeError` if it encounters an invalid control character. This is useful if you want to ensure that the JSON string is valid before attempting to parse it.

#### Section 4: Conclusion

In conclusion, if a JSON string contains an invalid control character, `json.loads()` will raise a `JSONDecodeError`. To handle this error, the invalid control character can either be removed from the string or the `strict` parameter can be used to cause `json.loads()` to raise an error if it encounters an invalid control character.
