---
title: What is the difference between a null value and a "not provided" value when performing a partial update using a spring rest controller?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: A null value should be used to indicate that a field should be removed, while a `not provided` value should be used to indicate that the field should remain unchanged.
---

**Contents**

[TOC]

1. Using Default Values

When a request for a partial update arrives, the controller can check for the presence of the value in the request. If the value is not present, the controller can set a default value for the property. This will allow the controller to distinguish between a null value and a value that was not provided.

2. Using Optional Parameters

Another approach is to use optional parameters. The controller can check for the presence of the optional parameter in the request. If the parameter is not present, it can be assumed that the value was not provided.

3. Using a Separate Flag

A third approach is to use a separate flag to indicate whether a value was provided or not. For example, a boolean flag can be included in the request to indicate whether a value was provided or not. The controller can then use this flag to determine whether the value was provided or not.

4. Using a Separate Field

A fourth approach is to use a separate field to indicate whether a value was provided or not. For example, a boolean field can be included in the request to indicate whether a value was provided or not. The controller can then use this field to determine whether the value was provided or not.
