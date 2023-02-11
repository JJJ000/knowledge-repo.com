---
title: Retrofit expected an object to be present, but an array was encountered instead
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Retrofit can`t parse the JSON because it is expecting an object, but the JSON is an array.
---

**Contents**

[TOC]

## Solution

### Deserializing JSON

When deserializing JSON, Retrofit expects the response body to conform to the structure of the model class. If the JSON response contains an array instead of an object, the deserialization will fail.

### Fixing the Issue

To fix the issue, you can either change the structure of the model class to match the JSON response, or you can modify the JSON response to match the model class.

### Changing the Model Class

If the JSON response contains an array instead of an object, you can modify the model class to match the structure of the JSON response. This can be done by adding a wrapper class that contains an array of the model class.

### Modifying the JSON Response

If the JSON response contains an array instead of an object, you can modify the response to match the model class. This can be done by wrapping the array in an object.
