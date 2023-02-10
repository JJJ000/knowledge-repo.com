---
title: Using simple JSON library, how can I read a JSON file into java?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSONObject class from the simple JSON library to read a JSON file into Java.
---

**Contents**

[TOC]

##### Step 1: Add the Dependency
Add the following dependency to the `pom.xml` file:
```
<dependency>
    <groupId>com.googlecode.json-simple</groupId>
    <artifactId>json-simple</artifactId>
    <version>1.1.1</version>
</dependency>
```

##### Step 2: Read the JSON File
Create a `FileReader` object to read the JSON file:
```
FileReader reader = new FileReader("path/to/file.json");
```

##### Step 3: Parse the JSON File
Use the `JSONParser` to parse the file:
```
JSONParser parser = new JSONParser();
Object obj = parser.parse(reader);
```

##### Step 4: Access the JSON Data
Cast the parsed object to a `JSONObject` and access the data:
```
JSONObject jsonObject = (JSONObject) obj;
String name = (String) jsonObject.get("name");
int age = (int) jsonObject.get("age");
```
