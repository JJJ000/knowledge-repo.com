---
title: What is the best way to return a JSON response from a symfony2 controller?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Return a new JsonResponse object from the controller.
---

**Contents**

[TOC]

1. Create a Response
First, create a Response object with the json content:

```php
$response = new Response(json_encode($data));
$response->headers->set('Content-Type', 'application/json');
```

2. Return the Response
Then return the Response object from the controller action:

```php
return $response;
```

3. Set the Response Status Code
Optionally, you can set the response status code:

```php
$response->setStatusCode(200);
```

4. Configure the Serializer
Finally, if you're using the Symfony Serializer component, you can configure it to return the response in JSON format:

```php
$serializer = $this->get('serializer');
$response = new Response($serializer->serialize($data, 'json'));
```
