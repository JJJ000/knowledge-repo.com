---
title: Generating JSON from a PHP script
authors:
- cool_wizard
tags:
- json
- php
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A PHP script can return JSON by using the `json_encode()` function.
---

**Contents**

[TOC]

### Setting the Content-Type Header

When returning a JSON response from a PHP script, the first step is to set the content type to `application/json`. This is done by setting the `Content-Type` header, like so:

```php
header('Content-Type: application/json');
```

### Generating the JSON Data

Next, we need to generate the actual JSON data. This can be done using the `json_encode()` function, which takes an array or object as an argument and returns the encoded JSON string.

For example, if we had an array of data that we wanted to encode, we could do the following:

```php
$data = array('foo' => 'bar', 'baz' => 'qux');
$json = json_encode($data);
```

### Sending the Response

Finally, we need to send the JSON response to the client. This is done using the `echo` statement, like so:

```php
echo $json;
```

### Putting it All Together

Putting it all together, the complete PHP script for returning a JSON response would look like this:

```php
header('Content-Type: application/json');

$data = array('foo' => 'bar', 'baz' => 'qux');
$json = json_encode($data);

echo $json;
```
