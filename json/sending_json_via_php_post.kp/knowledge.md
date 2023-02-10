---
title: Send a php-formatted JSON post
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the PHP function `file\_get\_contents()` to send a JSON post request.
---

**Contents**

[TOC]

## Creating the Data

The first step is to create the data that you want to send. This can be done by creating an associative array, which will store the data in key-value pairs.

```php
$data = array(
    'name' => 'John Doe',
    'email' => 'john@example.com',
    'phone' => '555-123-4567',
);
```

## Encode the Data

Once the data is created, it must be encoded into a JSON string to be sent in the post request. This can be done using the `json_encode()` function in PHP.

```php
$json_data = json_encode($data);
```

## Create the Request

The next step is to create the request. This can be done using the `curl_init()` function to create a cURL object.

```php
$curl = curl_init();
```

## Send the Request

Finally, the request can be sent using the `curl_setopt()` function to set the necessary options and the `curl_exec()` function to execute the request.

```php
curl_setopt($curl, CURLOPT_URL, 'http://example.com/api/');
curl_setopt($curl, CURLOPT_POST, true);
curl_setopt($curl, CURLOPT_POSTFIELDS, $json_data);
curl_setopt($curl, CURLOPT_RETURNTRANSFER, true);

$response = curl_exec($curl);
```
