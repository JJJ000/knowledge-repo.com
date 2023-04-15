---
title: Retrieve a compilation of materials from the classpath folder
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the ClassLoader.getResources() method to get a list of resources from a classpath directory in Java.
---

**Contents**

[TOC]

### Get the Resources

The following code snippet can be used to get a list of resources from a classpath directory in Java:

```java
ClassLoader classLoader = Thread.currentThread().getContextClassLoader();
URL url = classLoader.getResource(path);
File directory = new File(url.getFile());
File[] files = directory.listFiles();
```

### Iterate Through the Resources

Once the list of resources is retrieved, it can be iterated through using a for loop:

```java
for (File file : files) {
    // do something with the file
}
```

### Check for Resources

In order to check if there are any resources in the classpath directory, the length of the `files` array can be checked:

```java
if (files.length > 0) {
    // do something
}
```

### Get the Resource Name

To get the name of a resource file, the `getName()` method can be used:

```java
String fileName = file.getName();
```
