---
title: Retrieve data from a JSON file using php
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: PHP can be used to retrieve data from a JSON file using the json\_decode() function.
---

**Contents**

[TOC]

## Reading the JSON File

To read a JSON file using PHP, you will need to use the `file_get_contents` function. This function reads the contents of a file into a string. The following example reads the contents of a JSON file into a string:

```php
$json = file_get_contents('data.json');
```

## Decoding the JSON

Once the JSON file has been read into a string, it can be decoded using the `json_decode` function. This function takes a JSON string and returns an array or object. The following example decodes the JSON string into an associative array:

```php
$data = json_decode($json, true);
```

## Accessing the Data

Once the JSON data has been decoded, it can be accessed using array or object notation. The following example accesses an element in the array:

```php
echo $data['name']; // Outputs "John Doe"
```

## Error Handling

When decoding JSON, it is important to check for errors. The `json_last_error` function can be used to check for errors. The following example checks for errors and throws an exception if an error is found:

```php
if (json_last_error() !== JSON_ERROR_NONE) {
    throw new Exception('Error decoding JSON: ' . json_last_error_msg());
}
```
