---
title: The method 'optstring()' of a JSON object returns the string value 'null' if no value is associated with the specified key
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, jsonObject.optString() will return the String `null` if the key does not exist in the JSON object.
---

**Contents**

[TOC]

**Yes**

**Explanation**

When a `JSONObject` does not contain a value for the specified key, the `optString()` method will return the String `"null"`. This is different from `getString()`, which will throw a `JSONException` if the key does not exist.
