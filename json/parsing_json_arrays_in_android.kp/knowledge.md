---
title: What is the process for parsing a JSON array in android?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSONArray class to parse a JSON Array in Android.
---

**Contents**

[TOC]

1. **Using Android SDK (API Level 19 and above):**

- Use the `org.json.JSONArray` class to parse a JSON Array.
- Create a `JSONArray` object using the `JSONArray(String)` constructor.
- Iterate through the `JSONArray` object using the `getJSONObject(int)` method to get the individual `JSONObject`s from the array.
- Use the `optString(String)` method to get the value of the key from the `JSONObject`s.

2. **Using Third-Party Libraries:**

- Use a third-party library such as Gson or Jackson to parse a JSON Array.
- Create a `JsonArray` object using the `JsonArray(String)` constructor.
- Iterate through the `JsonArray` object using the `getJsonObject(int)` method to get the individual `JsonObject`s from the array.
- Use the `getString(String)` method to get the value of the key from the `JsonObject`s.

3. **Using Native Android Code:**

- Use the `org.json.JSONObject` class to parse a JSON Array.
- Create a `JSONObject` object using the `JSONObject(String)` constructor.
- Iterate through the `JSONObject` object using the `getJSONArray(String)` method to get the individual `JSONArray`s from the object.
- Use the `getString(int)` method to get the value of the key from the `JSONArray`s.

4. **Using Java 8 Stream API:**

- Use the `java.util.stream.Stream` class to parse a JSON Array.
- Create a `Stream` object using the `Stream.of(String)` method.
- Iterate through the `Stream` object using the `map(Function)` method to get the individual `JSONObject`s from the array.
- Use the `getString(String)` method to get the value of the key from the `JSONObject`s.
