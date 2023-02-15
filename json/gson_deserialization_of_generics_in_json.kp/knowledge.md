---
title: Unpacking generic types using gson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: GSON can be used to deserialize generic types by using the TypeToken class.
---

**Contents**

[TOC]

## Section 1: Introduction
Gson is a Java library that is used for serializing and deserializing Java objects from and to JSON. It can be used to convert a Java object to JSON and vice versa. Gson is also capable of deserializing generic types. In this article, we will discuss how to deserialize generic types with Gson.

## Section 2: Deserializing Generic Types
Deserializing generic types with Gson is relatively straightforward. Gson can be used to deserialize a generic type by using the fromJson() method. This method takes a JSON string and a generic type as parameters. It then returns an object of the specified generic type.

The following example shows how to deserialize a generic type using Gson:

```
Type listType = new TypeToken<List<String>>(){}.getType();
List<String> list = gson.fromJson(jsonString, listType);
```

In the above example, we are deserializing a List of Strings from a JSON string. The TypeToken is used to create a type object which specifies the generic type of the object to be deserialized.

## Section 3: Deserializing Nested Generic Types
Gson can also be used to deserialize nested generic types. This is done by using the TypeToken class to create a type object which specifies the nested generic type. The following example shows how to deserialize a nested generic type using Gson:

```
Type mapType = new TypeToken<Map<String, List<Integer>>>(){}.getType();
Map<String, List<Integer>> map = gson.fromJson(jsonString, mapType);
```

In the above example, we are deserializing a Map of Strings to Lists of Integers from a JSON string. The TypeToken is used to create a type object which specifies the nested generic type.

## Section 4: Conclusion
In this article, we discussed how to deserialize generic types with Gson. We saw how to deserialize a generic type and a nested generic type. Gson is a powerful library that makes it easy to serialize and deserialize Java objects to and from JSON.
