---
title: Retrieving the http request body from a JSON post in php
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: In PHP, the JSON POST request body can be read using the json\_decode() function.
---

**Contents**

[TOC]

**Section 1: Retrieving the Request Body**

The request body of an HTTP POST request can be accessed using the `php://input` stream. This stream contains raw data that is sent in the body of the request. To read this data as a JSON object, use `json_decode()`:

```php
$request_body = json_decode(file_get_contents('php://input'));
```

**Section 2: Validating the Request Body**

It is important to validate the request body to ensure that the data is valid and expected. This can be done using `json_last_error()` to check for any errors while decoding the JSON.

```php
if (json_last_error() !== JSON_ERROR_NONE) {
    // handle error
}
```

**Section 3: Accessing the Request Data**

Once the request body has been validated, the data can be accessed by looping through the object.

```php
foreach ($request_body as $key => $value) {
    // do something with the data
}
```

**Section 4: Error Handling**

It is important to handle any errors that may occur while reading or validating the request body. This can be done by checking the return value of `json_decode()` and `json_last_error()` and handling any errors appropriately.
