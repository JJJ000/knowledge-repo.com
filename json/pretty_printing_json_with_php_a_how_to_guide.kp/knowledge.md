---
title: How to print JSON in a readable format with PHP?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: PHP's `json_encode()` function can be used to pretty-print JSON.
---

**Contents**

[TOC]

### Encoding JSON

PHP provides the `json_encode` function which can be used to quickly and easily convert an array or object into a valid JSON string. This function takes the data as an argument, and returns the JSON-encoded string.

### Pretty-Printing

Pretty-printing is the process of formatting a JSON string so that it is easier for humans to read. This can be done with the `json_encode` function by passing in the `JSON_PRETTY_PRINT` option as a second argument. This will return a string with properly indented lines and whitespace.

### Example

For example, the following code will take an array and encode it into a JSON string with proper indentation:

```php
$data = [
    'name' => 'John',
    'age' => 30
];

$json = json_encode($data, JSON_PRETTY_PRINT);
```

The resulting `$json` string would look like this:

```json
{
    "name": "John",
    "age": 30
}
```
