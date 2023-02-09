---
title: Jquery.parsejson produces an "invalid json" error if a single quote is escaped in the json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: jQuery.parseJSON will throw an `Invalid JSON` error if the JSON string contains an escaped single quote.
---

**Contents**

[TOC]

1. What is jQuery.parseJSON?

jQuery.parseJSON is a method of the jQuery library which is used to parse a JSON string and convert it into a JavaScript object. It is used to convert a JSON string into a JavaScript object.

2. What Causes an "Invalid JSON" Error?

An "Invalid JSON" error is caused when the JSON string is not properly formatted. This can happen when there are missing or extra characters, or when the JSON string has an escaped single quote.

3. What is an Escaped Single Quote?

An escaped single quote is a character that is preceded by a backslash. This is done to indicate that the character should be interpreted as part of the string and not as the end of the string.

4. How to Avoid the Error?

To avoid the error, make sure that the JSON string is properly formatted and that all single quotes are properly escaped. Additionally, it is best to use a JSON validator to check the syntax of the JSON string before using it in your code.
