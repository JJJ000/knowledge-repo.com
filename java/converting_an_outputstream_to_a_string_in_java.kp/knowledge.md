---
title: Convert an outputstream into a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The OutputStream can be converted to a String using the toString() method of the ByteArrayOutputStream class.
---

**Contents**

[TOC]

### Option 1: Use ByteArrayOutputStream

ByteArrayOutputStream can be used to write the contents of an OutputStream to a String. It is a subclass of OutputStream, so it can be used with any OutputStream. 

To use ByteArrayOutputStream, create an instance of it, write to it using the OutputStream's write() method, and then get the written contents as a String by calling the ByteArrayOutputStream's toString() method.

### Example

Below is an example of how to use ByteArrayOutputStream to get an OutputStream into a String:

```java
try (ByteArrayOutputStream baos = new ByteArrayOutputStream()) {
    // write to the OutputStream
    baos.write("Hello World".getBytes());

    // get the written contents as a String
    String outputString = baos.toString();
}
```

### Option 2: Use IOUtils

Apache Commons IO's IOUtils class can also be used to write the contents of an OutputStream to a String. It provides a static method, toString(), which takes an OutputStream and returns the contents as a String.

### Example

Below is an example of how to use IOUtils to get an OutputStream into a String:

```java
try (OutputStream os = new ByteArrayOutputStream()) {
    // write to the OutputStream
    os.write("Hello World".getBytes());

    // get the written contents as a String
    String outputString = IOUtils.toString(os);
}
```
