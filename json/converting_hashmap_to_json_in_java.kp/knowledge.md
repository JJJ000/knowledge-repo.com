---
title: What is the process for transforming a hashmap into a JSON object in java?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the JSONObject class to convert a HashMap to a JSONObject.
---

**Contents**

[TOC]

### Section 1: Import Dependencies

In order to convert a hashmap to a JSON object in Java, you will need to import the JSON library. This can be done by adding the following line of code to your program:

```
import org.json.JSONObject;
```

### Section 2: Create a HashMap

Next, create a HashMap that contains the key-value pairs you want to convert to a JSON object. For example:

```
HashMap<String,String> map = new HashMap<>();
map.put("name", "John");
map.put("age", "25");
map.put("city", "New York");
```

### Section 3: Convert HashMap to JSON Object

Once you have created your HashMap, you can convert it to a JSON object using the following code:

```
JSONObject jsonObject = new JSONObject(map);
```

### Section 4: Print JSON Object

Finally, you can print out the JSON object using the following code:

```
System.out.println(jsonObject);
```

This will print out the JSON object in a readable format.
