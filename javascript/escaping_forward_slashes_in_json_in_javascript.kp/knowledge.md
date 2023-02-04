---
title: What is the purpose of escaping forward slashes when using json?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Forward slashes are escaped in Javascript to prevent any potential conflicts with string delimiters.
---

**Contents**

[TOC]

## Reason

Forward slashes are used to denote the beginning and end of a string in Javascript. Therefore, they need to be escaped in order to be used as a character within the string.

## Escape Character

The escape character in Javascript is the backslash (\). This character is used to indicate that the following character should be interpreted as a literal character, instead of having a special meaning.

## Escaping Forward Slashes

In order to use a forward slash as a literal character within a string, it must be escaped with a backslash. This will cause the forward slash to be interpreted as a literal character, instead of having a special meaning.

## Example

For example, the following string:

`"This is a string with a forward slash \/"`

will be interpreted as:

`This is a string with a forward slash /`
