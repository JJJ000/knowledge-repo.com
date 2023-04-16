---
title: Regular expressions for jquery selectors
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery selector regular expressions in Javascript are used to match a set of elements in a document.
---

**Contents**

[TOC]

1. Basics:

The most basic syntax for a jQuery selector is a simple string containing one or more CSS selectors separated by commas. The syntax for a jQuery selector regular expression is a string containing a regular expression pattern, optionally followed by one or more flags.

2. Flags:

Flags are used to modify the behavior of the regular expression pattern. The most commonly used flags are "g" (global match) and "i" (case-insensitive match).

3. Examples:

The following are some examples of jQuery selector regular expressions:

`/^([a-zA-Z0-9_\-\.]+)@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)|(([a-zA-Z0-9\-]+\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\]?)$/i`

This regular expression pattern matches a valid email address.

`/^(#|\.)?([a-zA-Z0-9_-]+)$/g`

This regular expression pattern matches a valid HTML element ID or class name.

4. Resources:

For more information on jQuery selector regular expressions, please refer to the official jQuery documentation here: http://api.jquery.com/category/selectors/jquery-selector-regexp/
