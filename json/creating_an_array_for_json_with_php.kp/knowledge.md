---
title: What is the syntax for creating an array in PHP to store JSON data?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the json\_encode() function to create an array for JSON using PHP.
---

**Contents**

[TOC]

### Section 1 - Create the Array

To create an array for JSON using PHP, you can use the `json_encode()` function. This function takes an array as an argument, and returns a string containing the JSON representation of the array.

```php
$myArray = array('foo' => 'bar', 'baz' => 'qux');
$myJSON = json_encode($myArray);
```

### Section 2 - Formatting the Array

You can also use the `json_encode()` function to format the array in a specific way. For example, you can use the `JSON_PRETTY_PRINT` option to add whitespace and indentation to the JSON string.

```php
$myJSON = json_encode($myArray, JSON_PRETTY_PRINT);
```

### Section 3 - Adding Options

You can also add additional options to the `json_encode()` function. For example, you can use the `JSON_UNESCAPED_SLASHES` option to prevent backslashes from being escaped in the JSON string.

```php
$myJSON = json_encode($myArray, JSON_PRETTY_PRINT | JSON_UNESCAPED_SLASHES);
```

### Section 4 - Handling Errors

It's important to handle any errors that might occur when using the `json_encode()` function. The function returns `FALSE` if an error occurs, so you should check the return value before using the JSON string.

```php
$myJSON = json_encode($myArray, JSON_PRETTY_PRINT);
if ($myJSON === FALSE) {
    // Handle the error
}
```
