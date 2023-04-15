---
title: Loading a list from a properties file using the spring @value annotation
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using the @Value annotation, a list can be read from a properties file and loaded into a Java application.
---

**Contents**

[TOC]

### Reading a List from Properties File

Properties files are used to store configuration data in key-value pairs. To read a list from a properties file, the list must first be stored in the file in a comma-separated format. For example, a list of colors can be stored in the properties file like this: 

```
colors=red,green,blue
```

### Load with Spring Annotation @Value

The Spring framework provides the @Value annotation to inject values from a properties file into a Java class. To inject a list from a properties file, the @Value annotation must be used with the `#{'${key}'.split(',')}` syntax, where `key` is the key of the list from the properties file. For example, to inject the list of colors from the properties file above, the @Value annotation should be used like this:

```
@Value("#{'${colors}'.split(',')}")
private List<String> colors;
```

### Using the Injected List

The injected list can then be used in the Java class like any other list. For example, to print out the list of colors, the following code can be used:

```
for (String color : colors) {
    System.out.println(color);
}
```

### Example

The following is an example of a Java class that uses the @Value annotation to inject a list from a properties file:

```
@Component
public class MyClass {

    @Value("#{'${colors}'.split(',')}")
    private List<String> colors;

    public void printColors() {
        for (String color : colors) {
            System.out.println(color);
        }
    }
}
```
