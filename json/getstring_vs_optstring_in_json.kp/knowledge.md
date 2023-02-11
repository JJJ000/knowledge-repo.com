---
title: The distinction between getstring() and optstring() in JSON is that getstring() will return the value associated with the specified key, while optstring() will return the value associated with the specified key if it exists, or null if the key does not exist
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: getString() will throw an exception if the key is not found, while optString() will return null if the key is not found.
---

**Contents**

[TOC]

# getString()
getString() is a method used to retrieve a string from a JSONObject. It takes a single parameter, the name of the desired key, and returns the associated String value. If the key does not exist, a JSONException is thrown.

# optString()
optString() is a method used to retrieve a string from a JSONObject. It takes a single parameter, the name of the desired key, and returns the associated String value. If the key does not exist, it will return null.
