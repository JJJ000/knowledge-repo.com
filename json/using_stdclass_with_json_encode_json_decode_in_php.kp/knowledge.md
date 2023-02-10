---
title: Php's json_encode/json_decode functions will return an instance of the stdclass object instead of an array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: json\_encode/json\_decode returns objects as stdClass instead of associative arrays by default.
---

**Contents**

[TOC]

## Introduction

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write, and easy for machines to parse and generate. PHP provides functions for encoding and decoding JSON data. The `json_encode()` function is used to convert PHP data into JSON formatted data and the `json_decode()` function is used to convert JSON data into PHP data.

## Why Does json_encode/json_decode Return stdClass Instead of Array?

When `json_decode()` is used to decode a JSON string, the resulting data structure is a PHP `stdClass` object. This is because most of the data structures in JSON are objects, and `stdClass` is the default object type in PHP.

The `stdClass` object is a generic object type that is used when no other object type is specified. It is often used to represent an associative array, or a collection of key-value pairs.

## How to Convert stdClass to Array

The `json_decode()` function can be used to convert a JSON string into an array. By passing `true` as the second argument to `json_decode()`, the resulting data structure will be an associative array instead of an `stdClass` object.

```php
$json = '{"foo":"bar"}';
$array = json_decode($json, true);

echo $array['foo']; // Outputs "bar"
```

## Conclusion

The `json_encode()` and `json_decode()` functions are used to convert between JSON and PHP data structures. By default, `json_decode()` will return a `stdClass` object. However, passing `true` as the second argument to `json_decode()` will convert the data structure into an array.
