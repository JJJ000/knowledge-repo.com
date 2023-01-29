---
title: What is the command to find the current working directory in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The current working directory can be obtained using the System.getProperty(`user.dir`) method.
---

**Contents**

[TOC]

### Using System.getProperty()

The System.getProperty() method can be used to retrieve the current working directory in Java. This method takes a single argument, a String representing the system property, and returns the value of the specified property.

### Example Code

The following code example demonstrates how to use the System.getProperty() method to retrieve the current working directory in Java:

```java
String currentWorkingDir = System.getProperty("user.dir");
System.out.println("Current working directory : " + currentWorkingDir);
```

### Output

The above code will output the following:

```java
Current working directory : /path/to/current/working/directory
```

### Additional Information

It is important to note that the System.getProperty() method returns the value of the specified property as a String, and not as a File object. As such, it is important to be aware of the platform-dependent path separator when constructing paths using the returned value.
