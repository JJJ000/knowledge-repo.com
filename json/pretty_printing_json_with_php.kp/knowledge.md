---
title: Formatting JSON output with php's json_encode function
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, json\_encode does not `pretty print` json.
---

**Contents**

[TOC]

# Section 1: Pretty Print JSON with PHP

Pretty printing JSON with PHP can be done using the `json_encode()` function. This function will take a PHP variable, array, or object and convert it into a JSON string. The `json_encode()` function also has an optional parameter which allows for a more readable output.

# Section 2: Enabling Pretty Print

To enable pretty print, the second parameter of the `json_encode()` function must be set to `JSON_PRETTY_PRINT`. This will cause the JSON output to be formatted with proper indentation and line breaks.

# Section 3: Example

Below is an example of using the `json_encode()` function with the `JSON_PRETTY_PRINT` parameter:

```php
$data = array(
    "name" => "John Doe",
    "age" => 30
);

$json = json_encode($data, JSON_PRETTY_PRINT);

echo $json;
```

The above code will output the following JSON:

```json
{
    "name": "John Doe",
    "age": 30
}
```

# Section 4: Conclusion

Pretty printing JSON with PHP can be done by using the `json_encode()` function with the `JSON_PRETTY_PRINT` parameter. This will result in a more readable JSON output which can be easier to debug and work with.
