---
title: Iterating through a JSON array in android/java
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Loop through the JSON Array using a for loop, accessing each element using the index.
---

**Contents**

[TOC]

### 1. Using for Loop 

We can use a for loop to iterate over a JSONArray in Android/Java. The following code snippet shows how this can be done:

```java
JSONArray array = new JSONArray(jsonString);
for (int i = 0; i < array.length(); i++) {
    JSONObject object = array.getJSONObject(i);
    // Do something with the object
}
```

### 2. Using Iterator 

We can also use an Iterator to iterate over a JSONArray in Android/Java. The following code snippet shows how this can be done:

```java
JSONArray array = new JSONArray(jsonString);
Iterator<Object> iterator = array.iterator();
while (iterator.hasNext()) {
    JSONObject object = (JSONObject) iterator.next();
    // Do something with the object
}
```

### 3. Using forEach 

We can also use a forEach loop to iterate over a JSONArray in Android/Java. The following code snippet shows how this can be done:

```java
JSONArray array = new JSONArray(jsonString);
array.forEach(item -> {
    JSONObject object = (JSONObject) item;
    // Do something with the object
});
```

### 4. Using Stream API 

We can also use the Stream API to iterate over a JSONArray in Android/Java. The following code snippet shows how this can be done:

```java
JSONArray array = new JSONArray(jsonString);
array.stream().forEach(item -> {
    JSONObject object = (JSONObject) item;
    // Do something with the object
});
```
