---
title: How to construct a valid jsonarray in Java using jsonobject
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Create a JSONArray object, and add JSONObjects to it using the add() method.
---

**Contents**

[TOC]

**Section 1: Install JSON Library**

In order to create a JSONArray in Java, you will need to install a JSON library such as Jackson or Gson. 

**Section 2: Create JSONObject**

Once the library is installed, you can create a JSONObject by instantiating it with the library's JSONObject class. For example:

```
JSONObject jsonObject = new JSONObject();
```

**Section 3: Populate JSONObject**

Next, you can populate the JSONObject by adding key-value pairs. For example:

```
jsonObject.put("name", "John");
jsonObject.put("age", 30);
```

**Section 4: Create JSONArray**

Finally, you can create a JSONArray by instantiating it with the library's JSONArray class. You can then add the JSONObject to the JSONArray. For example:

```
JSONArray jsonArray = new JSONArray();
jsonArray.add(jsonObject);
```
