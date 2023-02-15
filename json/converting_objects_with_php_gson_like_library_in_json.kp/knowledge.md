---
title: Transforming objects to and from JSON format in PHP (similar to the gson library in java)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: In PHP, the json\_encode() and json\_decode() functions can be used to convert objects to and from JSON.
---

**Contents**

[TOC]

# Section 1: Converting Object to JSON in PHP

Objects in PHP can be converted to JSON using the `json_encode()` function. This function will take an object as an argument and return a JSON-encoded string.

Example:

```
<?php
$obj = new stdClass();
$obj->name = "John";
$obj->age = 30;
$obj->city = "New York";

echo json_encode($obj);
?>
```

Output:

```
{"name":"John","age":30,"city":"New York"}
```

# Section 2: Converting JSON to Object in PHP

JSON strings can be converted to objects in PHP using the `json_decode()` function. This function will take a JSON-encoded string as an argument and return an object.

Example:

```
<?php
$json = '{"name":"John","age":30,"city":"New York"}';

$obj = json_decode($json);

echo $obj->name;
?>
```

Output:

```
John
```

# Section 3: Libraries for JSON in PHP

There are a few libraries available for working with JSON in PHP. Some popular ones include:

* [json_decode()](https://github.com/joshcam/PHP-JSON-Decode)
* [json_encode()](https://github.com/joshcam/PHP-JSON-Encode)
* [JsonMapper](https://github.com/mahmoudz/jsonmapper)

# Section 4: Comparison to Gson for Java

The libraries mentioned above are similar to the [Gson](https://github.com/google/gson) library for Java in that they provide a way to convert JSON strings to objects and vice versa. However, unlike Gson, they do not provide additional features such as serializing and deserializing objects to and from JSON.
