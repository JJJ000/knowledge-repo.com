---
title: What is the cause of json.parse not working with an empty string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON.parse fails with the empty string in JSON because it is not valid JSON syntax.
---

**Contents**

[TOC]

# Empty String

The empty string is an invalid value in JSON. JSON.parse will fail when attempting to parse an empty string because it does not conform to the syntax rules of JSON.

# Syntax Rules

JSON is a text-based format for representing structured data. It has strict syntax rules which must be followed in order for it to be valid. The empty string does not conform to these syntax rules and therefore cannot be parsed by the JSON.parse function.

# Parsing Error

When attempting to parse an empty string, JSON.parse will throw a SyntaxError. This error indicates that the string does not conform to the syntax rules of JSON and cannot be parsed.

# Alternatives

If an empty string is required, it can be represented in JSON as a null value. This will allow the string to be parsed by the JSON.parse function.
