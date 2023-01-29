---
title: Retrieve a string outside of a context or activity
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is not possible to get a String outside of a Context or Activity in Java.
---

**Contents**

[TOC]

#Using System Properties

System properties are key-value pairs that are available to all parts of the Java application. They can be accessed through the System class.

####Accessing System Properties

System properties are accessed using the `System.getProperty()` method. This method takes a single argument, the key of the property you want to retrieve.

####Setting System Properties

System properties can be set using the `System.setProperty()` method. This method takes two arguments, the key and the value of the property you want to set.

####Example

The following example shows how to set and get a system property:

```java
String propertyKey = "myProperty";
String propertyValue = "myValue";

// Set the property
System.setProperty(propertyKey, propertyValue);

// Get the property
String retrievedValue = System.getProperty(propertyKey);

System.out.println("Retrieved value: " + retrievedValue);
```

The output of the above example will be:

```
Retrieved value: myValue
```
