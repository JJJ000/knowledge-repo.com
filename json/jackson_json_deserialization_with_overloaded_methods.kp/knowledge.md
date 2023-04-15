---
title: Converting JSON into an object with overloaded methods using jackson's deserialization
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In order to deserialize JSON into an object with overloaded methods using Jackson, you will need to use the @JsonCreator annotation to specify which constructor or static factory method to use for deserialization.
---

**Contents**

[TOC]

## Overview
When deserializing JSON into an object with overloaded methods using Jackson, we need to use a combination of annotations and custom deserializers to make sure that Jackson correctly maps the JSON data to the appropriate method. This can be done in four main steps:

1. Define the object class with overloaded methods
2. Create custom deserializers for each overloaded method
3. Annotate the class and methods with Jackson annotations
4. Use the ObjectMapper to deserialize the JSON into the object

Let's take a closer look at each of these steps.

## Define the object class with overloaded methods
The first step is to define the object class with overloaded methods that we want to deserialize the JSON into. For example, let's say we have a class called `MyObject` with two methods called `setValue` that take different parameter types:

```java
public class MyObject {
  private String value;

  public void setValue(String value) {
    this.value = value;
  }

  public void setValue(int value) {
    this.value = Integer.toString(value);
  }
}
```

## Create custom deserializers for each overloaded method
Since Jackson can't automatically determine which method to call based on the parameter type, we need to create custom deserializers for each overloaded method. To do this, we need to extend the `JsonDeserializer` class and implement the `deserialize` method. Here's an example deserializer for the `setValue` method that takes a string parameter:

```java
public class SetValueStringDeserializer extends JsonDeserializer<Void> {

  @Override
  public Void deserialize(JsonParser p, DeserializationContext ctxt) throws IOException, JsonProcessingException {
    MyObject myObject = (MyObject) ctxt.getAttribute("MyObject");
    myObject.setValue(p.getText());
    return null;
  }
}
```

Note that we're using the `DeserializationContext` object to retrieve the `MyObject` instance that we're deserializing into.

We'll need to create a similar deserializer for the `setValue` method that takes an integer parameter.

## Annotate the class and methods with Jackson annotations
Next, we need to annotate the `MyObject` class and its methods with Jackson annotations to tell Jackson to use our custom deserializers. Here's what the final class and method annotations should look like:

```java
@JsonDeserialize(using = MyObjectDeserializer.class)
public class MyObject {
  private String value;

  @JsonDeserialize(using = SetValueStringDeserializer.class)
  public void setValue(String value) {
    this.value = value;
  }

  @JsonDeserialize(using = SetValueIntDeserializer.class)
  public void setValue(int value) {
    this.value = Integer.toString(value);
  }
}
```

Note that we're using the `@JsonDeserialize` annotation to specify our custom deserializers for each method.

## Use the ObjectMapper to deserialize the JSON into the object
Finally, we can use the `ObjectMapper` to deserialize the JSON into our `MyObject` instance:

```java
ObjectMapper objectMapper = new ObjectMapper();
MyObject myObject = objectMapper.readValue(jsonString, MyObject.class);
```

Jackson will now use our custom deserializers to correctly map the JSON data to the appropriate method based on the parameter type.

And that's it! With these four steps, we can deserialize JSON into an object with overloaded methods using Jackson.
