---
title: Jq not functioning correctly when processing tag names containing dashes and numbers
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: No, jQuery does not support tag names with dashes and numbers in JSON.
---

**Contents**

[TOC]

# Section 1: JSON Syntax

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data between different applications. It is based on a subset of the JavaScript programming language and is composed of two parts: an object, which is a collection of key-value pairs, and an array, which is an ordered list of values.

# Section 2: jq Syntax

jq is a command-line JSON processor that is used to parse, filter, and transform JSON data. It is written in C and uses a syntax similar to JavaScript, but it is not a programming language. It supports a wide variety of operations, including mapping, filtering, and sorting.

# Section 3: Tag Names with Dashes and Numbers

When using jq to query JSON data, tag names with dashes and numbers can be used. jq supports a wide range of characters in its syntax, including dashes and numbers. However, the syntax must be properly formatted for the jq command to work correctly.

# Section 4: Proper Syntax

In order to use tag names with dashes and numbers in jq, the proper syntax must be used. For example, if a tag name contains a dash, it must be enclosed in quotation marks. Similarly, if it contains a number, the number must be preceded by a backslash.
