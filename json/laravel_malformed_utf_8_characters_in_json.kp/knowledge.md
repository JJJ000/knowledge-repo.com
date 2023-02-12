---
title: Incorrectly encoded characters in the utf-8 format, which may be malformed
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The response should be encoded as UTF-8 to prevent the `Malformed UTF-8 characters, possibly incorrectly encoded` error in Laravel when returning JSON.
---

**Contents**

[TOC]

# Overview 
When trying to return a response with a JSON payload in Laravel, you may encounter an error that says "Malformed UTF-8 characters, possibly incorrectly encoded". This error occurs when the response contains characters that cannot be correctly encoded in UTF-8.

# Causes
This error occurs when the response contains characters that cannot be correctly encoded in UTF-8. This could be due to a number of reasons, including:
- Incorrectly encoded characters in the source data
- Non-UTF-8 characters in the source data
- Incorrectly encoded characters in the database
- Characters that are not supported by UTF-8

# Solutions
There are a few solutions to this problem:
- Ensure that all data is correctly encoded in UTF-8 before being inserted into the database.
- Use the `utf8_encode()` function to convert any non-UTF-8 characters to UTF-8.
- Use the `mb_convert_encoding()` function to convert any non-UTF-8 characters to UTF-8.
- Use the `iconv()` function to convert any non-UTF-8 characters to UTF-8.
