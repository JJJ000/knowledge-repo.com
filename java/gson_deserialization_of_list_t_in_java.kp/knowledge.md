---
title: Convert a list<t> object into its equivalent JSON representation using gson
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Gson can deserialize a List<T> object by calling the fromJson() method on a Gson object, passing in the JSON string and the type of the list.
---

**Contents**

[TOC]

### Deserializing a List<T>

1. Create a Gson object: 

```java
Gson gson = new Gson();
```

2. Deserialize the JSON string into a List<T> object:

```java
Type listType = new TypeToken<List<T>>(){}.getType();
List<T> list = gson.fromJson(jsonString, listType);
```

3. Iterate through the List<T> object:

```java
for (T item : list) {
    // Do something with the item
}
```

4. (Optional) Use the GsonBuilder to customize the deserialization:

```java
Gson gson = new GsonBuilder()
        // Customization options here
        .create();
```
