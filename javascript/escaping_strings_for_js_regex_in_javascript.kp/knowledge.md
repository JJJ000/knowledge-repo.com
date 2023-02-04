---
title: Create a string that can be used safely in a JavaScript regular expression
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `String.prototype.replace()` method to escape special characters in the string to be used in a Javascript regex.
---

**Contents**

[TOC]

#### Step 1: Escape All Relevant Characters

Relevant characters to escape include `^$.*+?=!:|\/()[]{}`.

#### Step 2: Add Backslashes

To escape these characters, add a backslash `\` before each character.

#### Step 3: Add Delimiters

To make the string a valid regex expression, add delimiters such as `/` at the beginning and end of the string.

#### Step 4: Wrap in Quotes

Finally, wrap the entire expression in quotes so that it can be used as a string in Javascript.
