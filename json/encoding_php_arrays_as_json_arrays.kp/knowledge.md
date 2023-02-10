---
title: Convert a PHP array into a JSON array, not a JSON object, using json_encode
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `JSON\_FORCE\_OBJECT` flag when encoding the array.
---

**Contents**

[TOC]

##### Option 1:
1. Create an array in PHP:
```
$arr = array('a' => 1, 'b' => 2, 'c' => 3, 'd' => 4, 'e' => 5);
```
2. Use `json_encode()` to convert the array to a JSON array:
```
$json_arr = json_encode($arr, JSON_FORCE_OBJECT);
```
3. Print the JSON array:
```
echo $json_arr;
```

##### Option 2:
1. Create an array in PHP:
```
$arr = array('a' => 1, 'b' => 2, 'c' => 3, 'd' => 4, 'e' => 5);
```
2. Use `json_encode()` to convert the array to a JSON array:
```
$json_arr = json_encode($arr, JSON_FORCE_OBJECT);
```
3. Convert the JSON array to a JSON object:
```
$json_obj = json_decode($json_arr);
```
4. Print the JSON object:
```
echo $json_obj;
```
