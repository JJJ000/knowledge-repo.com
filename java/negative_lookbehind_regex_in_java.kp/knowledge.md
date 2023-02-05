---
title: Regex for finding something if it does not have something else before it
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The regex would be `(?!somethingelse).*` to match anything that is not preceded by `somethingelse`.
---

**Contents**

[TOC]

## Regex
`(?!<preceding-string>)<matching-string>`

## Explanation
This regex matches a `<matching-string>` only if it is not preceded by a `<preceding-string>`.

## Example 
For example, if we want to match the string "apple" only if it is not preceded by the string "orange", we can use the following regex: `(?!orange)apple`.
