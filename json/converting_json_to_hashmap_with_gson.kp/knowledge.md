---
title: What is the process for transforming a JSON object into a hashmap using gson?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can convert JSON to a HashMap using Gson by calling Gson`s fromJson() method.
---

**Contents**

[TOC]

1. Adding Dependency 
In order to use Gson, you need to add the following dependency to your project:

```
compile 'com.google.code.gson:gson:2.8.5'
```

2. Creating Gson Object 
Once the dependency is added, you can create a Gson object to use in your application.

```
Gson gson = new Gson();
```

3. Parsing JSON 
Now you can parse the JSON string into a Java object or a HashMap.

```
String jsonString = "{\"name\":\"John\",\"age\":30}";
HashMap<String, Object> map = gson.fromJson(jsonString, new TypeToken<HashMap<String, Object>>(){}.getType());
```

4. Accessing Values 
You can now access the values from the HashMap.

```
String name = map.get("name");
int age = map.get("age");
```
