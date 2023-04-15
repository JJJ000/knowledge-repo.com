---
title: What is the syntax for returning an http 400 error in a spring mvc @responsebody method that returns a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Return a ResponseEntity with a status of HttpStatus.BAD\_REQUEST and a body containing the desired error message.
---

**Contents**

[TOC]

### Step 1: Create an Error Response Object

Create an `ErrorResponse` object which can be used to return an HTTP 400 error in the response body. This object should have fields such as `code`, `message`, and `details`, which will contain the relevant information for the error.

### Step 2: Return the Response

Return the `ErrorResponse` object from the `@ResponseBody` method, using the `ResponseEntity` class. This will allow you to set the appropriate HTTP status code (400) in the response.

### Step 3: Set the Response Status

Set the response status to `HttpStatus.BAD_REQUEST` when creating the `ResponseEntity` object. This will ensure that the response is sent with the correct HTTP status code.

### Step 4: Return the Response as JSON

Finally, return the `ErrorResponse` object as JSON. This can be done by using the `ResponseEntity` `.ok()` method and passing in the `ErrorResponse` object as a parameter. This will ensure that the response is sent in the correct format.
