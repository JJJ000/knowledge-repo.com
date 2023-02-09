---
title: Convert xml to JSON using php
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: PHP can convert XML to JSON using the json\_encode() function.
---

**Contents**

[TOC]

# Section 1

PHP provides a built-in function called `json_encode` which can be used to convert an XML string into a JSON string.

# Section 2

Using `json_encode` is simple. All that needs to be done is to pass the XML string to the `json_encode` function and it will return the JSON string.

# Section 3

An example of how to use `json_encode` is shown below:

```php
$xmlString = '<root><node>value</node></root>';
$jsonString = json_encode($xmlString);
```

# Section 4

The `json_encode` function also accepts an array of options that can be used to customize the output. These options include `JSON_PRETTY_PRINT`, `JSON_UNESCAPED_SLASHES`, and `JSON_UNESCAPED_UNICODE`. 
For more information on these options, please refer to the [PHP documentation](https://www.php.net/manual/en/function.json-encode.php).
