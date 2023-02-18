---
title: Change the default JSON error response from a spring boot rest controller
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The default JSON error response from a Spring Boot Rest Controller can be modified by creating a custom ErrorAttributes implementation.
---

**Contents**

[TOC]

## Modifying the Error Response

The default error response from a Spring Boot Rest Controller can be modified by making changes to the `ErrorAttributes` bean in the application configuration. This bean is responsible for providing the default error attributes that are included in the response.

## Customizing Error Attributes

The `ErrorAttributes` bean can be customized by implementing a custom `ErrorAttributes` class. This class can be used to add additional attributes to the response, such as a custom error code or a detailed error message.

## Adding Custom Error Handlers

In addition to customizing the `ErrorAttributes` bean, it is also possible to add custom error handlers to the application. These error handlers can be used to provide a more detailed response for specific types of errors.

## Overriding Default Error Response

Finally, it is also possible to completely override the default error response by implementing a custom `ErrorController` class. This class can be used to provide a custom response for all errors, regardless of the type.
