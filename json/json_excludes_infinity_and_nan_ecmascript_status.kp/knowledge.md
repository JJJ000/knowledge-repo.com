---
title: What is the status of infinity and nan in json, and how does it relate to ecmascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: JSON is supported as a native data type in ECMAScript, but does not include Infinity and NaN.
---

**Contents**

[TOC]

# Section 1: JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging data between different systems. It is a text-based format that is language independent, and can be easily read and written by humans. JSON is based on a subset of the JavaScript programming language, and is commonly used to store and exchange data between web applications and servers.

# Section 2: Infinity and NaN

Infinity and NaN (Not a Number) are two special values used in the JavaScript programming language. Infinity is a special value that represents an infinitely large number, while NaN is a special value that represents an undefined or unrepresentable value. These values are not supported by JSON, as they are not valid JavaScript values.

# Section 3: ECMAScript

ECMAScript is the official standard for the JavaScript programming language. It is maintained by the European Computer Manufacturers Association (ECMA), and is used as the basis for the official JavaScript specification. ECMAScript includes support for Infinity and NaN, as they are valid values in JavaScript.

# Section 4: JSON in ECMAScript

JSON is not part of the official ECMAScript standard, as it is not a valid JavaScript value. However, JSON is widely used in web applications and servers, and is supported by most modern web browsers. As such, many JavaScript libraries and frameworks include support for parsing and generating JSON data.
