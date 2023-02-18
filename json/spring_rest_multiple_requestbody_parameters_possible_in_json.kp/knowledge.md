---
title: Is it possible to have multiple @requestbody parameters in a spring rest application?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Yes, it is possible to have multiple @RequestBody parameters in a JSON request.
---

**Contents**

[TOC]

1. Overview

2. RequestBody Parameters

3. JSON Format

4. Conclusion

## Overview

REST (Representational State Transfer) is an architectural style for developing web services. It is often used in combination with the HTTP protocol to provide a simple and consistent interface for clients to access and manipulate web resources.

The @RequestBody annotation is used to bind request body parameters to a method argument in a Spring MVC controller. It can be used to bind multiple parameters at once, and can be used to bind parameters of different types.

## RequestBody Parameters

The @RequestBody annotation can be used to bind multiple parameters to a method argument. Each parameter will be bound to a separate argument in the method, and the parameters can be of different types. For example, the following controller method binds two parameters, an integer and a string, to two separate method arguments:

```
@PostMapping
public void handleRequest(@RequestBody int id, @RequestBody String name) {
  // handle request
}
```

## JSON Format

When using the @RequestBody annotation, the parameters must be in a valid JSON format. This means that each parameter must be in the form of a key-value pair, with the key being the parameter name and the value being the parameter value.

For example, if we wanted to bind the two parameters in the previous example, we would need to send a JSON object with the following structure:

```
{
  "id": 123,
  "name": "John Doe"
}
```

## Conclusion

Yes, it is possible to use the @RequestBody annotation to bind multiple parameters to a method argument in a Spring MVC controller. The parameters must be provided in a valid JSON format, with each parameter being a key-value pair.
