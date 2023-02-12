---
title: A JSON object is not recognized in internet explorer 8
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Internet Explorer 8 does not support JSON natively, so any JSON objects will be undefined.
---

**Contents**

[TOC]

**Section 1: What is JSON?**

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing structured data based on JavaScript object syntax.

**Section 2: What is the Issue?**

In Internet Explorer 8, JSON objects are not supported, which means that any code using JSON objects will not work.

**Section 3: What is the Solution?**

The solution is to use a polyfill library such as json2.js or es5-shim.js to add support for JSON objects in Internet Explorer 8.

**Section 4: How to Implement the Solution?**

In order to implement the solution, the polyfill library needs to be included in the HTML page. This can be done by adding a script tag pointing to the library, or by including the library in the page’s JavaScript file. Once the library is included, the JSON object will be supported in Internet Explorer 8.
