---
title: The json.loads function in Python is throwing a valueerror because there is additional data present
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The JSON data provided is invalid and needs to be corrected before it can be parsed.
---

**Contents**

[TOC]

# Introduction

The `json.loads()` function is part of the Python standard library and is used to convert a string into a valid JSON object. It is a powerful tool for working with JSON data, but it can also lead to errors if the data is not properly formatted. One of the most common errors encountered when using `json.loads()` is the ValueError: Extra data? error. 

# Causes of ValueError: Extra Data?

The ValueError: Extra data? error is caused when the string passed to `json.loads()` contains extra data that is not valid JSON. This can be caused by a variety of issues, including incorrect formatting, missing commas, or mismatched quotes.

# Solutions

The most effective way to resolve this error is to check the formatting of the string to ensure it is valid JSON. If there are any extra characters, mismatched quotes, or missing commas, they should be removed or corrected. Additionally, it is important to check for any trailing whitespace, as this can also cause the ValueError: Extra data? error.

Once the formatting has been checked and corrected, the string should be passed to `json.loads()` again to see if the error is resolved. If the error persists, it is likely that the string is not valid JSON and should be further investigated.
