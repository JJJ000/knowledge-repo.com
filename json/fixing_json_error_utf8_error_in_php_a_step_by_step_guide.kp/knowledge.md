---
title: What is the solution for addressing json_error_utf8 error when using PHP json_decode?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use mb\_convert\_encoding() function to convert the input string to UTF-8 before calling json\_decode().
---

**Contents**

[TOC]

## Introduction
JSON is an acronym for JavaScript Object Notation, and it is a standard data exchange format. `json_decode()` is a PHP function that is used to decode JSON-encoded strings into PHP objects or associative arrays. JSON-encoded data must be in UTF-8 format to be decoded correctly. Sometimes, you may encounter a JSON_ERROR_UTF8 error message when using `json_decode()`. This article will provide insights on how to solve JSON_ERROR_UTF8 error in php json_decode.

## Check for UTF-8 encoded data
JSON-encoded data must be in UTF-8 format to be decoded correctly. Therefore, the first step to take when encountering a JSON_ERROR_UTF8 error is to check whether the data passed to the `json_decode()` function is UTF-8 encoded. You can do this by using the `mb_detect_encoding()` function in PHP to detect the text encoding of the JSON string. Here is an example:

```
$jsonString = '{"name": "John", "age": 34, "city": "New York"}';

if (mb_detect_encoding($jsonString, 'UTF-8', true) === false) {
    echo 'Invalid encoding detected.';
} else {
    $result = json_decode($jsonString, true);
    var_dump($result);
}
```

## Fix invalid characters in the JSON string
If you have determined that the JSON string is not encoded in UTF-8 format, you can use the `utf8_encode()` function in PHP to convert it to UTF-8 format. Here is an example:

```
$jsonString = '{"name": "John √¢¬Ä¬ì", "age": 34, "city": "New York"}';

if (mb_detect_encoding($jsonString, 'UTF-8', true) === false) {
    $jsonString = utf8_encode($jsonString);
}

$result = json_decode($jsonString, true);
var_dump($result);
```

The `utf8_encode()` function will convert the string to UTF-8 format, and the `json_decode()` function will be able to decode the JSON-encoded data correctly.

## Use a JSON validation tool
If the data being passed to the `json_decode()` function is encoded in UTF-8 format, but you are still receiving a JSON_ERROR_UTF8 error message, you may have invalid characters in the JSON string. In this case, you can use a JSON validation tool to locate the invalid characters and fix them before attempting to decode the JSON string. Here are some useful JSON validation tools:

- JSONLint
- JSON Formatter & Validator
- JSON Compare

## Conclusion
In conclusion, JSON_ERROR_UTF8 error is a common error message that occurs when using the `json_decode()` function in PHP. This error message is caused by invalid or improperly encoded characters in the JSON string. By checking for proper UTF-8 encoding, fixing invalid characters, and using a JSON validation tool, you can successfully solve JSON_ERROR_UTF8 error in php json_decode.
