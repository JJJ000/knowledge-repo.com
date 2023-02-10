---
title: How to return a plain string as a JSON object in a rest controller using spring mvc
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Return a ResponseEntity with the String as the body and the appropriate headers set.
---

**Contents**

[TOC]

1. Implementing a REST Controller

To return a simple String as JSON in a Spring MVC Rest Controller, first create a controller class with the @RestController annotation. This annotation will enable the controller to handle requests and return responses in the JSON format.

2. Creating a Method to Return String as JSON

In the controller class, create a method that will return the String as JSON. This method should be annotated with the @ResponseBody annotation, which will indicate that the response should be in JSON format. The method should also accept a request parameter, which will be used to determine the value of the String that is returned.

3. Setting the Response Content Type

The response content type should be set to "application/json". This can be done by using the @RequestMapping annotation, which allows the response content type to be specified.

4. Returning the String as JSON

Finally, the String should be returned as JSON. This can be done by using the Jackson library, which provides a convenient way to convert a Java object to JSON. The String should be wrapped in a JSON object before being returned.
