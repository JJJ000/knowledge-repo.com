---
title: The @responsebody annotation in spring boot does not convert entity ids into a serialized format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The @ResponseBody annotation only serializes the fields of an entity, not its id.
---

**Contents**

[TOC]

**Section 1: Overview of @ResponseBody**

The @ResponseBody annotation is a Spring annotation used to bind a method return value to the web response body. It can be used to convert the return value of a controller method into a format suitable for the web. This annotation is often used in combination with the @RequestMapping annotation to create a RESTful web service.

**Section 2: How @ResponseBody Works**

When the @ResponseBody annotation is used, Spring automatically converts the return value of the method into a format suitable for the web. This is done using the HttpMessageConverter interface, which defines how to convert the return value into a format suitable for the web. By default, Spring uses the Jackson library to convert the return value into a JSON format.

**Section 3: Entity Id Not Serialized**

By default, the Jackson library used by Spring to convert the return value into a JSON format does not serialize the entity id. This is because the entity id is not a property of the entity, but rather a reference to the entity itself.

**Section 4: Solution**

To serialize the entity id, you can create a custom Jackson serializer. This serializer can be used to serialize the entity id as part of the JSON response. Alternatively, you can add the @JsonProperty annotation to the entity id field to indicate that it should be serialized as part of the JSON response.
