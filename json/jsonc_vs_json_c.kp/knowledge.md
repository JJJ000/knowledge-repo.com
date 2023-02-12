---
title: Could you explain to me the difference between jsonc and json-c?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: JSONC is a modified version of JSON that adds support for comments, while JSON-C is a C library for parsing and manipulating JSON data.
---

**Contents**

[TOC]

# What is JSONC

JSONC stands for JavaScript Object Notation with Comments. It is an extension of the JSON data interchange format that supports comments.

# How is it Different from JSON

JSONC is different from JSON in that it allows comments to be included in the data. Comments are enclosed in /* */ and are ignored by JSON parsers. This allows developers to include helpful documentation or notes in the data that will not be interpreted by the parser.

# Advantages of JSONC

The main advantage of JSONC is that it allows developers to include comments in the data without having to worry about the comments being interpreted by the parser. This makes it easier for developers to document their data and provide helpful information to other developers.

# Disadvantages of JSONC

The main disadvantage of JSONC is that it is not a standard format and is not supported by all JSON parsers. This means that developers must ensure that the parser they are using supports JSONC before using it. Additionally, JSONC can be more difficult to read and debug than standard JSON.
