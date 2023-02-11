---
title: Loop through a jsonarray in json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can iterate through a JSONArray in JSON by using a for loop.
---

**Contents**

[TOC]

**Section 1: Retrieve the JSONArray**

The first step is to retrieve the JSONArray from the JSON object. This can be done using the getJSONArray() method, passing in the key of the JSONArray.

```java
JSONArray array = jsonObject.getJSONArray("key");
```

**Section 2: Iterate Through the JSONArray**

Once the JSONArray is retrieved, it can be iterated through using a for loop. The loop should start at 0 and end at the length of the JSONArray.

```java
for (int i = 0; i < array.length(); i++) {
    // Get the JSONObject at the current index
    JSONObject obj = array.getJSONObject(i);
    // Do something with the JSONObject
}
```

**Section 3: Accessing Values**

Once the JSONObject is retrieved from the JSONArray, the values can be accessed using the appropriate getter method. For example, if the JSONObject has a String value with the key "name", the value can be retrieved using the getString() method:

```java
String name = obj.getString("name");
```

**Section 4: Updating Values**

Finally, if the values in the JSONObject need to be updated, the appropriate setter method can be used. For example, if the JSONObject has an Integer value with the key "age", the value can be updated using the put() method:

```java
obj.put("age", 18);
```
