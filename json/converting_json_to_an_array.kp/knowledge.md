---
title: Convert JSON to array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, json\_decode can be used to convert JSON data into an array.
---

**Contents**

[TOC]

#### Solution 1

```php
$data = json_decode($json);
$array = (array)$data;
```

#### Solution 2

```php
$array = json_decode($json, true);
```
