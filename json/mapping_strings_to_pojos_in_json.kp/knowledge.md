---
title: Transform a map<string, string> into a plain old Java object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use a JSON library to convert the Map to a JSON string, then use a JSON parser to convert the JSON string to a POJO.
---

**Contents**

[TOC]

### Section 1: Convert Map to Json String

The following code snippet can be used to convert a `Map<String, String>` to a JSON String:

```java
import com.fasterxml.jackson.databind.ObjectMapper;

Map<String, String> map = new HashMap<>();
map.put("key1", "value1");
map.put("key2", "value2");

ObjectMapper mapper = new ObjectMapper();
String jsonString = mapper.writeValueAsString(map);
```

### Section 2: Create POJO

A POJO (Plain Old Java Object) can be created from the JSON String using the following code snippet:

```java
import com.fasterxml.jackson.databind.ObjectMapper;

ObjectMapper mapper = new ObjectMapper();
MyPojo pojo = mapper.readValue(jsonString, MyPojo.class);
```

### Section 3: Define POJO

The POJO class `MyPojo` should be defined as follows:

```java
public class MyPojo {
    private String key1;
    private String key2;
    
    public String getKey1() {
        return key1;
    }
    
    public void setKey1(String key1) {
        this.key1 = key1;
    }
    
    public String getKey2() {
        return key2;
    }
    
    public void setKey2(String key2) {
        this.key2 = key2;
    }
}
```

### Section 4: Access POJO Values

The values of the POJO can be accessed using the following code snippet:

```java
String value1 = pojo.getKey1();
String value2 = pojo.getKey2();
```
