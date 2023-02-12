---
title: What is the syntax for filtering by string in jsonpath?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the `contains()` function to filter by string in JSONPath.
---

**Contents**

[TOC]

## Section 1: Understanding JSONPath
JSONPath is a query language for JSON documents. It is used to select specific elements from a JSON document. It is similar to XPath, which is used to select elements from an XML document.

## Section 2: Syntax
JSONPath uses a syntax similar to XPath, with a few differences. It uses the dollar sign ($) as the root object, and the dot (.) to access elements in the JSON document. Brackets ([]) are used to access array elements.

## Section 3: Filtering
Filtering is done using the square bracket ([]) syntax. The expression inside the square brackets is a boolean expression which is evaluated for each element in the array. If the expression evaluates to true, the element is included in the result.

## Section 4: Example
For example, the following JSONPath expression will select all elements in the array whose "name" property is equal to "John":

```
$.array[?(@.name == "John")]
```
