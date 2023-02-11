---
title: Manipulating information in a PHP JSON structure
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: In PHP, JSON objects can be handled by decoding the JSON string into a PHP associative array.
---

**Contents**

[TOC]

## Section 1: Retrieving Data from JSON Object

To retrieve data from a JSON object, you can use the `json_decode()` function. This function takes a JSON string and converts it into a PHP object. You can then access the data from the object using the `->` operator.

For example, to access the value of a key called `name` in a JSON object, you can use the following code:

```php
$jsonObj = json_decode($jsonString);
$name = $jsonObj->name;
```

## Section 2: Modifying Data in JSON Object

To modify data in a JSON object, you can use the `json_encode()` function. This function takes a PHP object and converts it into a JSON string. You can then modify the data in the object and re-encode it back into a JSON string.

For example, to modify the value of a key called `name` in a JSON object, you can use the following code:

```php
$jsonObj = json_decode($jsonString);
$jsonObj->name = 'New Name';
$jsonString = json_encode($jsonObj);
```

## Section 3: Adding Data to JSON Object

To add data to a JSON object, you can use the `json_decode()` and `json_encode()` functions. First, you can use `json_decode()` to convert the JSON string into a PHP object. Then, you can add new data to the object using the `[]` operator. Finally, you can use `json_encode()` to convert the PHP object back into a JSON string.

For example, to add a new key called `age` with a value of `25` to a JSON object, you can use the following code:

```php
$jsonObj = json_decode($jsonString);
$jsonObj->age = 25;
$jsonString = json_encode($jsonObj);
```

## Section 4: Removing Data from JSON Object

To remove data from a JSON object, you can use the `unset()` function. This function takes a key as an argument and removes the corresponding data from the object.

For example, to remove the key called `name` from a JSON object, you can use the following code:

```php
$jsonObj = json_decode($jsonString);
unset($jsonObj->name);
$jsonString = json_encode($jsonObj);
```
