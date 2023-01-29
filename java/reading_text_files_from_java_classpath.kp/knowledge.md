---
title: What is the process for reading a text file from the classpath in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The ClassLoader.getResourceAsStream() method can be used to read a text file from the classpath in Java.
---

**Contents**

[TOC]

### Using getResourceAsStream()

The getResourceAsStream() method of the Class class can be used to read a text file from the classpath. This method takes a string argument that represents the path of the resource to be read. It returns an InputStream object which can be used to read the contents of the file.

### Using getResource()

The getResource() method of the Class class can also be used to read a text file from the classpath. This method takes a string argument that represents the path of the resource to be read. It returns a URL object which can be used to get an InputStream object which can be used to read the contents of the file.

### Example

Let's say we have a text file named "sample.txt" in the classpath. We can read this file using the following code:

```java
InputStream inputStream = getClass().getResourceAsStream("/sample.txt");
BufferedReader br = new BufferedReader(new InputStreamReader(inputStream));
String line;
while ((line = br.readLine()) != null) {
    System.out.println(line);
}
```

### Conclusion

In conclusion, we can use the getResourceAsStream() and getResource() methods of the Class class to read a text file from the classpath in Java.
