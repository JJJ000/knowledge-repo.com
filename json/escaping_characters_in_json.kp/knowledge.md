---
title: Rewording 'json and escaping characters'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: JSON requires that certain characters, such as quotation marks, be escaped with a backslash character in order to be valid.
---

**Contents**

[TOC]

**Section 1: What is JSON?**
JSON stands for JavaScript Object Notation. It is a lightweight data-interchange format that is used to store and exchange data between different applications. JSON is based on a subset of the JavaScript programming language, and is easy for humans to read and write.

**Section 2: Why Escaping Characters in JSON is Necessary?**
When using JSON, it is important to escape characters in order to ensure that the data is correctly interpreted by the receiving application. This is especially true when dealing with special characters such as quotation marks, backslashes, and other non-alphanumeric characters. Escaping these characters helps to prevent potential security issues and data corruption.

**Section 3: What Characters Need to be Escaped?**
The characters that need to be escaped in JSON include quotation marks, backslashes, and other non-alphanumeric characters. Additionally, certain control characters such as newlines and tabs need to be escaped as well.

**Section 4: How to Escape Characters in JSON?**
The escaping of characters in JSON is done using the backslash character (\). For example, a quotation mark would be escaped as \", and a backslash as \\. Additionally, certain control characters such as newlines and tabs need to be escaped as well. For example, a newline would be escaped as \n.
