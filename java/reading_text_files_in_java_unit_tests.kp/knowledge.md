---
title: What is the process for importing a text-file into a Java unit test?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A text-file resource can be read into a Java unit test using the ClassLoader.getResourceAsStream() method.
---

**Contents**

[TOC]

### 1. Create a Resource File

Create a text file with the content you would like to read. This file should be stored in the same directory as your Java unit test.

### 2. Add Resource File to Build Path

Add the resource file to your project's build path so that it is accessible to your unit test. In Eclipse, this can be done by right-clicking on the resource file, selecting Build Path > Add to Build Path.

### 3. Read Resource File

Create a `BufferedReader` object to read the resource file. Use the `ClassLoader` object to get the resource file's path.

```java
ClassLoader classLoader = getClass().getClassLoader();
File file = new File(classLoader.getResource("resource_file.txt").getFile());
BufferedReader br = new BufferedReader(new FileReader(file));
```

### 4. Process Resource File

Once the `BufferedReader` object has been created, you can process the file line by line. For example, you can use a `while` loop to read each line and store the content in a `String` variable.

```java
String line;
while ((line = br.readLine()) != null) {
   // process the line
}
```
