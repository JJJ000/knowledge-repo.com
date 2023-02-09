---
title: What is the process for retrieving and using information from a JSON file using php?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Using the json\_decode() function, you can extract and access data from JSON with PHP.
---

**Contents**

[TOC]

### Section 1: Decode JSON

The first step in extracting and accessing data from a JSON object is to decode the JSON object. This can be done with the `json_decode()` function in PHP.

### Section 2: Access Data

Once the JSON object has been decoded, the data can be accessed by using the `$object->key` syntax. For example, if the JSON object contains a key called "name", the value of that key can be accessed by using `$object->name`.

### Section 3: Iterate Through Data

If the JSON object contains an array, the data can be iterated through using `foreach` loops. For example, if the JSON object contains an array of objects called "users", the data can be iterated through by using the following code:

```php
foreach ($object->users as $user) {
    // do something with each user
}
```

### Section 4: Retrieve Data

Once the data has been accessed and iterated through, it can be retrieved by using the `$object->key` syntax. For example, if the JSON object contains an object with a key called "name", the value of that key can be retrieved by using `$object->name`.
