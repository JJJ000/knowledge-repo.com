---
title: Making a patch request with resttemplate
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: To make a PATCH request in Json using RestTemplate, use the exchange() method with the PATCH HttpMethod and a valid JSON request body.
---

**Contents**

[TOC]

#### Section 1: Overview

PATCH is an HTTP method that can be used to update existing resources. It is often used when only a few fields of a resource need to be updated, as opposed to PUT which is used to replace the entire resource.

When making a PATCH request with a RestTemplate, the request body should contain a JSON object with the fields that need to be updated.

#### Section 2: RestTemplate

The RestTemplate class is a part of the Spring framework and provides methods for making HTTP requests. To make a PATCH request with the RestTemplate, the `patchForObject()` method can be used. This method takes a URI, a request body, and a response type as parameters.

#### Section 3: JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is commonly used for sending data over the internet. To make a PATCH request with the RestTemplate, the request body should be a JSON object containing the fields that need to be updated.

#### Section 4: Example

For example, if we want to update the name of a user with ID 123, the request body should look like this:

```
{
  "id": 123,
  "name": "John Doe"
}
```

And the RestTemplate code would look like this:

```
String uri = "http://example.com/users/123";
User user = new User(123, "John Doe");
User updatedUser = restTemplate.patchForObject(uri, user, User.class);
```
