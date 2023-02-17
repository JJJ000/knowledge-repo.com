---
title: Returning JSON data from a spring controller using @responsebody
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Return a Java object annotated with @ResponseBody to have it serialized into JSON using a Jackson2HttpMessageConverter.
---

**Contents**

[TOC]

1. Adding Dependencies
-----------------------

In order to return JSON data from a Spring Controller using @ResponseBody, you need to have the Jackson library included in your project. You can add the Jackson library as a dependency in your Maven project by adding the following to your `pom.xml` file:

```xml
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>2.9.8</version>
</dependency>
```

2. Configuring the Controller
-----------------------------

Next, you need to configure your Spring Controller to return JSON data. To do this, you need to add the `@ResponseBody` annotation to your Controller's methods. This will tell Spring to serialize the returned object into JSON and return it in the response.

For example, if you have a Controller with a method that returns an `Employee` object, you can add the `@ResponseBody` annotation like so:

```java
@RequestMapping("/employee")
public class EmployeeController {
    @ResponseBody
    @GetMapping
    public Employee getEmployee() {
        // code to retrieve employee
        return employee;
    }
}
```

3. Serializing the Object
-------------------------

Finally, you need to serialize the object that you are returning from the Controller. You can do this by using the Jackson library. Jackson is an open source library that can be used to serialize Java objects into JSON.

To serialize an object, you need to create an `ObjectMapper` instance and then call the `writeValueAsString()` method. For example, if you want to serialize an `Employee` object, you can do it like this:

```java
ObjectMapper mapper = new ObjectMapper();
String jsonString = mapper.writeValueAsString(employee);
```

4. Returning the JSON
---------------------

Once you have serialized the object, you can return it from the Controller method. You can do this by simply returning the JSON string that you just created:

```java
@RequestMapping("/employee")
public class EmployeeController {
    @ResponseBody
    @GetMapping
    public String getEmployee() {
        ObjectMapper mapper = new ObjectMapper();
        String jsonString = mapper.writeValueAsString(employee);
        return jsonString;
    }
}
```
