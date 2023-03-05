---
title: What is the process to enable Jackson to format rendered JSON in spring mvc for rest?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can enable Jackson to pretty-print rendered JSON by configuring the ObjectMapper bean with the property `INDENT\_OUTPUT` set to true.
---

**Contents**

[TOC]

## Add Jackson Dependency

To enable Jackson for pretty-printing rendered JSON in Spring MVC, you first need to add the Jackson dependency to your project. You can do this by adding the following dependency to your `pom.xml` file if you're using Maven:

```xml
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>${jackson.version}</version>
</dependency>
```

Replace `${jackson.version}` with the version of Jackson you want to use.


## Configure Jackson ObjectMapper

Next, you need to configure the Jackson `ObjectMapper` to enable pretty-printing. You can do this by creating a `@Bean` method in one of your Spring configuration classes, like this:

```java
@Configuration
public class JacksonConfig {

    @Bean
    public ObjectMapper objectMapper() {
        ObjectMapper objectMapper = new ObjectMapper();
        objectMapper.enable(SerializationFeature.INDENT_OUTPUT);
        return objectMapper;
    }
}
```

This creates a new instance of `ObjectMapper` and enables the `SerializationFeature.INDENT_OUTPUT` feature, which enables pretty-printing for JSON output.


## Use Jackson ObjectMapper

Once you've configured the `ObjectMapper`, you can use it to serialize your response data to JSON. For example, if you have a controller method that returns a JSON response, you can annotate it with `@ResponseBody` and use the `ObjectMapper` to serialize the response:

```java
@Controller
public class MyController {

    @Autowired
    private ObjectMapper objectMapper;

    @GetMapping(value = "/my-endpoint", produces = MediaType.APPLICATION_JSON_VALUE)
    @ResponseBody
    public MyResponseData getMyData() {
        // get your response data
        MyResponseData data = new MyResponseData();

        // serialize the response to JSON using the ObjectMapper
        String json = null;
        try {
            json = objectMapper.writeValueAsString(data);
        } catch (JsonProcessingException e) {
            // handle exception
        }

        return json;
    }
}
```

In this example, we've injected the `ObjectMapper` into the controller using Spring's `@Autowired` annotation, and then used it to serialize the response data to JSON. The `produces` attribute of the `@GetMapping` annotation specifies that the response content type should be `application/json`.

## Conclusion

By adding the Jackson dependency, configuring the Jackson `ObjectMapper`, and using it to serialize your response data to JSON, you can enable pretty-printing for JSON output in Spring MVC.
