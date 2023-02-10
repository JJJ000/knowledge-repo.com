---
title: The function json.marshal when given a struct as an argument will return a string of "{}"
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: This happens when the struct is empty, meaning that all of its fields are zero-valued.
---

**Contents**

[TOC]

# Answer

## Scenario

In the scenario where a `struct` is passed as an argument to `json.Marshal()` and the return value is a `{}` empty JSON object, there could be a few possible explanations.

## Possible Explanations

1. The `struct` argument passed to `json.Marshal()` is empty. This could occur if the `struct` is an empty struct, or the struct has no fields defined. 
2. The `struct` argument passed to `json.Marshal()` contains fields, but the values of these fields are all empty. This could occur if the `struct` contains fields with empty values, such as an empty string, empty array, or `nil` values. 
3. The `struct` argument passed to `json.Marshal()` contains fields, but the values of these fields are not JSON-compatible types. This could occur if the `struct` contains fields with values that are not compatible with the JSON format, such as functions or pointers. 

## Conclusion

In conclusion, when `json.Marshal()` returns an empty JSON object `{}`, it is likely due to the `struct` argument being empty, containing empty values, or containing values of incompatible types.
