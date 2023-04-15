---
title: What is the process of assigning object field names that are different from JSON field names?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `@JsonProperty` annotation with the desired object field name as the value parameter to map the JSON field to the object field.
---

**Contents**

[TOC]

## Introduction
JSON (JavaScript Object Notation) is a popular data format used for exchanging data between web services and clients. JSON objects consist of key-value pairs, where the key is a string and the value can be a string, number, boolean, null, array or another JSON object. In some cases, the field names in the JSON objects may not match the field names in the client-side or server-side objects. In such cases, we need to map the JSON field names to different object field names. This can be achieved using various techniques as discussed below.

## Using Annotations
One way to map JSON field names to different object field names is by using annotations. Annotations are special metadata added to the code that provide additional information about the program elements to the compiler or runtime environment. In Java, for example, we can use the `@JsonProperty` annotation from the Jackson library to map JSON field names to object field names.

```java
public class Person {
    @JsonProperty("firstName")
    private String name;

    @JsonProperty("age")
    private int age;

    // getters and setters
}
```
In the above code, we have used the `@JsonProperty` annotation to map the JSON field names `"firstName"` and `"age"` to the object field names `name` and `age` respectively.

## Using Custom Deserializers
Another way to map JSON field names to different object field names is by using custom deserializers. A deserializer is a program that converts JSON data into a Java object. By creating a custom deserializer, we can have full control over the deserialization process, including the field name mapping.

```java
public class PersonDeserializer extends JsonDeserializer<Person> {
    @Override
    public Person deserialize(JsonParser jsonParser, DeserializationContext deserializationContext) throws IOException {
        ObjectCodec codec = jsonParser.getCodec();
        JsonNode node = codec.readTree(jsonParser);

        String firstName = node.get("firstName").asText();
        int age = node.get("age").asInt();

        Person person = new Person();
        person.setName(firstName);
        person.setAge(age);

        return person;
    }
}
```
In the above code, we have created a custom deserializer for the `Person` class. Inside the `deserialize` method, we first read the JSON tree using the `codec` object. Then, we map the JSON field names `"firstName"` and `"age"` to the object field names `name` and `age` respectively. Finally, we create a new `Person` object and set its fields using the mapped values.

## Using ObjectMapper
The third way to map JSON field names to different object field names is by using the `ObjectMapper` class from the Jackson library. The `ObjectMapper` class provides various methods to customize the serialization and deserialization process, including the field name mapping.

```java
ObjectMapper mapper = new ObjectMapper();
mapper.setPropertyNamingStrategy(PropertyNamingStrategy.SNAKE_CASE);

Person person = mapper.readValue(jsonString, Person.class);
```
In the above code, we have created a new `ObjectMapper` object and set the `propertyNamingStrategy` to `SNAKE_CASE`. This means that the JSON field names will be converted to snake_case before mapping to object field names. Finally, we use the `readValue` method to deserialize the JSON string into a `Person` object with the mapped field names.

## Conclusion
In conclusion, we learned about different techniques to map JSON field names to different object field names. We can use annotations, custom deserializers, or the `ObjectMapper` class from the Jackson library to achieve this. The choice of technique depends on the specific use case and requirements of the application.
