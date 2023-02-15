---
title: Encoding of incorrectly formatted utf-8 characters in PHP json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The json\_encode() function will return a JSON encoded string containing an error if the input contains invalid UTF-8 characters.
---

**Contents**

[TOC]

# Introduction
PHP has a built-in function called `json_encode()` which is used to convert a PHP value to a JSON string. This function is often used to encode data for use in AJAX requests. However, if the data contains malformed UTF-8 characters, it can cause issues when attempting to encode the data. This article will explain what malformed UTF-8 characters are and how to address them when using PHP's `json_encode()` function.

# What are Malformed UTF-8 Characters?
UTF-8 is a character encoding system that is used to represent text in a variety of languages. It is the most widely used character encoding system on the web, and it is the default encoding system for HTML5. Malformed UTF-8 characters are characters that don't conform to the UTF-8 standard. This can happen when data is transferred from one system to another, or when the data is manually entered by a user. 

# How to Address Malformed UTF-8 Characters with json_encode()
The best way to address malformed UTF-8 characters when using PHP's `json_encode()` function is to use the `JSON_PARTIAL_OUTPUT_ON_ERROR` option. This option allows the function to return a partial JSON string if it encounters an encoding error. This way, the JSON string will still be valid, but any malformed characters will be omitted.

# Conclusion
Malformed UTF-8 characters can cause issues when attempting to encode data with PHP's `json_encode()` function. The best way to address this issue is to use the `JSON_PARTIAL_OUTPUT_ON_ERROR` option, which will allow the function to return a partial JSON string if it encounters an encoding error.
