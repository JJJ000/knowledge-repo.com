---
title: Retrieving post data in JSON format using php
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: PHP can read a JSON POST request using the json\_decode() function.
---

**Contents**

[TOC]

# Section 1: Reading JSON POST

To read a JSON POST in PHP, you can use the `json_decode()` function. This function takes a string as an argument and returns an object or an array of the JSON data.

# Section 2: Example

For example, if you have the following JSON POST:

```
{
    "name": "John Doe",
    "age": 30
}
```

You can read it using the `json_decode()` function like this:

```php
$data = json_decode($_POST['data']);

$name = $data->name;
$age = $data->age;
```

# Section 3: Error Handling

It is important to note that if the JSON POST is invalid, `json_decode()` will return `NULL`. Therefore, it is important to check for errors before attempting to access the data.

# Section 4: Additional Resources

For more information on `json_decode()` and other JSON functions in PHP, please refer to the [PHP JSON Documentation](https://www.php.net/manual/en/book.json.php).
