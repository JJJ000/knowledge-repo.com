---
title: What is the syntax for setting a value to null with org.json.jsonobject in java?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the put() method to set a value to null with org.json.JSONObject in Java.
---

**Contents**

[TOC]

**Setting a Value to Null**

1. Create a JSONObject: 
   Create a JSONObject to store the key-value pair.

```Java
JSONObject jsonObject = new JSONObject();
```

2. Set the Value to Null: 
   Use the `put` method to set the value to `null`.

```Java
jsonObject.put("key", null);
```

3. Get the Value: 
   Use the `get` method to get the value.

```Java
Object value = jsonObject.get("key");
```

4. Check if Value is Null: 
   Check if the value is `null` using the `==` operator.

```Java
if (value == null) {
    // Value is null
}
```
