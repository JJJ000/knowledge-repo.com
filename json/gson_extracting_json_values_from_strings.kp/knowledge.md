---
title: Retrieve JSON value from string using gson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the Gson library`s fromJson() method to get a JSON value from a String in JSON.
---

**Contents**

[TOC]

## Section 1: Using Gson

Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object.

To get a JSON value from a String in JSON, we can use the fromJson() method of the Gson class. This method takes a JSON string and a class object and returns an instance of the specified class object with the data from the JSON string.

For example, we can use the following code to get a JSON value from a String in JSON:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";

Gson gson = new Gson();
Person person = gson.fromJson(jsonString, Person.class);
System.out.println(person.getName()); // Prints "John"
System.out.println(person.getAge()); // Prints 30
```

## Section 2: Using JSONObject

JSONObject is a Java library that can be used to parse and manipulate JSON data. It provides a convenient way to access and manipulate JSON data.

To get a JSON value from a String in JSON, we can use the get() method of the JSONObject class. This method takes a String argument which is the key of the value to be retrieved and returns the corresponding value.

For example, we can use the following code to get a JSON value from a String in JSON:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";

JSONObject jsonObject = new JSONObject(jsonString);
String name = jsonObject.getString("name");
int age = jsonObject.getInt("age");
System.out.println(name); // Prints "John"
System.out.println(age); // Prints 30
```

## Section 3: Using Jackson

Jackson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object.

To get a JSON value from a String in JSON, we can use the readValue() method of the ObjectMapper class. This method takes a JSON string and a class object and returns an instance of the specified class object with the data from the JSON string.

For example, we can use the following code to get a JSON value from a String in JSON:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";

ObjectMapper mapper = new ObjectMapper();
Person person = mapper.readValue(jsonString, Person.class);
System.out.println(person.getName()); // Prints "John"
System.out.println(person.getAge()); // Prints 30
```

## Section 4: Using JsonNode

JsonNode is a Java library that can be used to parse and manipulate JSON data. It provides a convenient way to access and manipulate JSON data.

To get a JSON value from a String in JSON, we can use the get() method of the JsonNode class. This method takes a String argument which is the key of the value to be retrieved and returns the corresponding value.

For example, we can use the following code to get a JSON value from a String in JSON:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";

ObjectMapper mapper = new ObjectMapper();
JsonNode jsonNode = mapper.readTree(jsonString);
String name = jsonNode.get("name").asText();
int age = jsonNode.get("age").asInt();
System.out.println(name); // Prints "John"
System.out.println(age); // Prints 30
```
