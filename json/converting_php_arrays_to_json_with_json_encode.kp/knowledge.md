---
title: Convert a PHP array to a JSON array using json_encode();
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: json\_encode() can be used to convert a PHP array to a JSON array.
---

**Contents**

[TOC]

## Section 1: PHP Array

```php
$myArray = array('a' => 1, 'b' => 2, 'c' => 3, 'd' => 4, 'e' => 5);
```

## Section 2: JSON Array

```json
{"a":1,"b":2,"c":3,"d":4,"e":5}
```

## Section 3: Using json_encode

```php
$myJSON = json_encode($myArray);
```

## Section 4: Result

```json
{"a":1,"b":2,"c":3,"d":4,"e":5}
```
