---
title: How do JSON and JavaScript objects differ?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON is a text-based data interchange format, while a JavaScript object is a collection of unordered properties.
---

**Contents**

[TOC]

# Syntax
JSON has a more strict syntax than a JavaScript object. JSON requires double quotes around all property names, and all strings must be in double quotes. A JavaScript object does not require quotes around the property names, and strings can be in single or double quotes.

# Data Types
JSON only supports the following data types: strings, numbers, booleans, objects, arrays, and null. JavaScript objects can also include functions and dates.

# Parsing
JSON must be parsed with a JSON parser, while JavaScript objects can be parsed with eval() or the Function constructor.

# Usage
JSON is typically used to transfer data between a server and a web application, while JavaScript objects are used to store and manipulate data within the application.
