---
title: How do substr and substring differ?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The main difference between substr and substring in Javascript is that substr takes a start index and a length as parameters, while substring takes two indexes as parameters.
---

**Contents**

[TOC]

#### Definition

substr: Returns a portion of a string based on the starting index and the number of characters.

substring: Returns a portion of a string based on the starting and ending index.

#### Syntax 

substr: string.substr(start [, length ])

substring: string.substring(start [, end ])

#### Use Cases

substr: Used when you need to extract a certain number of characters from a string, starting from a specific index.

substring: Used when you need to extract characters from a string between two specified indices.

#### Output

substr: The output is a new string that is a substring of the original string.

substring: The output is a new string that is a substring of the original string.
