---
title: Convert a list<t> object to its JSON representation using gson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: To deserialize a List<T> object with Gson in Json, use the fromJson() method.
---

**Contents**

[TOC]

#### Section 1: Create a List<T> Object

To create a List<T> object with Gson, you must first create a class that implements the `List<T>` interface. This class must have a constructor that takes a `TypeToken` parameter, which is used to specify the type of the list elements. The `TypeToken` class is a generic type that is used to capture the type of a generic type instance.

For example, to create a `List<String>` object:

```java
public class StringList extends ArrayList<String> {
    public StringList(TypeToken<String> typeToken) {
        super(typeToken);
    }
}
```

#### Section 2: Serialize the List<T> Object

To serialize the List<T> object, use the `Gson.toJson()` method. The `Gson.toJson()` method takes two parameters: the object to serialize and the type of the object.

For example, to serialize the `StringList` object:

```java
Gson gson = new Gson();
StringList stringList = new StringList(TypeToken.get(String.class));
String jsonString = gson.toJson(stringList, stringList.getClass());
```

#### Section 3: Deserialize the List<T> Object

To deserialize the List<T> object, use the `Gson.fromJson()` method. The `Gson.fromJson()` method takes two parameters: the JSON string to deserialize and the type of the object.

For example, to deserialize the `StringList` object:

```java
Gson gson = new Gson();
StringList stringList = gson.fromJson(jsonString, StringList.class);
```

#### Section 4: Use the Deserialized List<T> Object

Once the List<T> object is deserialized, it can be used like any other `List<T>` object. For example, to iterate over the elements of the `StringList` object:

```java
for (String str : stringList) {
    // Do something with str
}
```
