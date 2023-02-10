---
title: Return a JSON response along with an http status code in laravel
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can return a JSON response along with an http status code using the `response()->json()` method.
---

**Contents**

[TOC]

### Using the Response Helper
The [`response()`](https://laravel.com/docs/5.5/responses#the-response-helper) helper can be used to return a JSON response with an HTTP status code.

### Example

```php
return response()->json(['name' => 'Abigail', 'state' => 'CA'], 200);
```

### Using the Response Facade
The [`Response`](https://laravel.com/api/5.5/Illuminate/Http/Response.html) facade can also be used to return a JSON response with an HTTP status code.

### Example

```php
return Response::json(['name' => 'Abigail', 'state' => 'CA'], 200);
```
