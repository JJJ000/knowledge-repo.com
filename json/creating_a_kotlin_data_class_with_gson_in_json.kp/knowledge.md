---
title: Parsing JSON into a kotlin data class using gson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Gson can be used to deserialize a Kotlin data class from a JSON string.
---

**Contents**

[TOC]

1. Overview
------
Kotlin data classes are a great way to quickly create classes that are used to represent data. They provide a lot of features such as immutability, type-safety, and data binding. When combined with GSON, they can be used to quickly deserialize JSON into Kotlin data classes.

2. Setting up GSON
------
The first step in using GSON to deserialize JSON into Kotlin data classes is to set up the GSON library. This can be done by adding the following line to the build.gradle file:
```
implementation 'com.google.code.gson:gson:2.8.6'
```

3. Creating a Kotlin Data Class
------
Once GSON is set up, the next step is to create a Kotlin data class that will be used to represent the data from the JSON. This can be done by using the `data` keyword followed by the class name and the properties of the class. For example:

```
data class User(val name: String, val age: Int)
```

4. Deserializing JSON into a Kotlin Data Class
------
Once the Kotlin data class is created, GSON can be used to deserialize the JSON into the data class. This can be done by creating a Gson instance and then passing the JSON string into the `fromJson` method. For example:

```
val gson = Gson()
val user = gson.fromJson(jsonString, User::class.java)
```

The `user` variable will then contain an instance of the `User` data class with the data from the JSON.
