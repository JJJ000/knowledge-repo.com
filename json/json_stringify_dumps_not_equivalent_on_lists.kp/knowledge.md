---
title: Are the outputs of json.stringify in JavaScript and json.dumps in Python different when applied to a list?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: No, they are not equivalent, as JSON.stringify() converts a JavaScript object or value to a JSON string, while json.dumps() converts a Python object into a JSON string.
---

**Contents**

[TOC]

# JSON.stringify

JSON.stringify is a Javascript function which converts a Javascript object or value to a JSON string. It takes two parameters - the value to be converted and an optional replacer function which can be used to filter out values.

# json.dumps

json.dumps is a Python function which converts a Python object into a JSON string. It takes two parameters - the object to be converted and an optional separator string which can be used to separate the elements of the object.

# Difference

The key difference between JSON.stringify and json.dumps is that JSON.stringify is used to convert a Javascript object or value to a JSON string, while json.dumps is used to convert a Python object into a JSON string. This means that JSON.stringify will not work on a Python list, while json.dumps will not work on a Javascript list.
