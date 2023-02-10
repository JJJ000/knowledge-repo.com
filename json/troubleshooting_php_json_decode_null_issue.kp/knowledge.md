---
title: What is the reason that PHP json_decode() is returning null when given seemingly valid json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The JSON string may not be properly formatted or may contain invalid characters.
---

**Contents**

[TOC]

**Section 1: Overview**

PHP's `json_decode()` function is used to convert a JSON string into a PHP value. However, there are occasions when a seemingly valid JSON string will be returned as NULL by `json_decode()`. This can be confusing and frustrating, as it can be difficult to determine what is causing the issue.

**Section 2: Possible Causes**

There are several potential causes for `json_decode()` returning NULL with a seemingly valid JSON string. These include: 

- Unescaped special characters
- Incorrectly encoded strings
- Invalid UTF-8 characters
- Unclosed strings
- Trailing commas

**Section 3: Troubleshooting**

If `json_decode()` returns NULL with a seemingly valid JSON string, it is important to troubleshoot the issue in order to determine the cause. This can be done by using a JSON validator to check the JSON string for errors, or by using the `json_last_error()` function to check for any errors that may have occurred during the decoding process.

**Section 4: Conclusion**

In conclusion, `json_decode()` can occasionally return NULL with a seemingly valid JSON string. To resolve this issue, it is important to troubleshoot the issue in order to determine the cause. This can be done by using a JSON validator or the `json_last_error()` function.
