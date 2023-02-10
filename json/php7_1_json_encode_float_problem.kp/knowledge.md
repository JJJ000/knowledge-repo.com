---
title: Issue with float values when using json_encode() in php7.1
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: PHP 7.1 changed the way floats are encoded, which can cause issues with json\_encode().
---

**Contents**

[TOC]

# Introduction

The PHP 7.1 `json_encode()` function has been known to cause issues when encoding floating-point numbers. This issue can cause unexpected results when converting floating-point numbers to JSON strings. This article will discuss the issue in more detail and provide potential solutions.

# Issue Description

The issue with the PHP 7.1 `json_encode()` function is that it does not properly handle floating-point numbers. This can cause unexpected results when encoding floating-point numbers. For example, a number like `1.23` may be encoded as `1.2299999999999998`. This can lead to unexpected results when the JSON string is parsed by another application.

# Potential Solutions

There are several potential solutions to this issue. The first is to use a different version of PHP, such as PHP 7.2 or higher. This version of PHP has been updated to properly handle floating-point numbers when encoding them to JSON strings.

Another potential solution is to use a third-party library such as JSON-C. This library provides a more robust JSON encoding and decoding functionality and can be used to properly encode floating-point numbers.

Finally, if neither of these solutions is viable, it is possible to manually encode the floating-point numbers using the `number_format()` function. This function allows you to specify the number of decimal places to be encoded and can be used to ensure that the encoded number is accurate.

# Conclusion

The PHP 7.1 `json_encode()` function can cause issues when encoding floating-point numbers. This can lead to unexpected results when the JSON string is parsed by another application. Potential solutions to this issue include using a different version of PHP, using a third-party library, or manually encoding the floating-point numbers using the `number_format()` function.
