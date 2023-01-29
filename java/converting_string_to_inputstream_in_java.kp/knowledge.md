---
title: What is the process for changing a string to an inputstream in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the InputStream constructor that takes a String as an argument.
---

**Contents**

[TOC]

### Using ByteArrayInputStream 

The ByteArrayInputStream class can be used to create an InputStream from a String. This can be done by creating a byte array from the string and passing it to the ByteArrayInputStream constructor.

```
String myString = "This is a string";
InputStream is = new ByteArrayInputStream(myString.getBytes());
```

### Using StringReader

The StringReader class can also be used to create an InputStream from a String. This can be done by passing the String to the StringReader constructor and then creating an InputStream from the StringReader.

```
String myString = "This is a string";
StringReader sr = new StringReader(myString);
InputStream is = new ReaderInputStream(sr);
```

### Using InputStreamReader

The InputStreamReader class can be used to create an InputStream from a String. This can be done by passing the String to the InputStreamReader constructor and then creating an InputStream from the InputStreamReader.

```
String myString = "This is a string";
InputStreamReader isr = new InputStreamReader(myString);
InputStream is = new ReaderInputStream(isr);
```

### Using Apache Commons IO

The Apache Commons IO library also provides a utility method for creating an InputStream from a String. This can be done by using the IOUtils.toInputStream() method.

```
String myString = "This is a string";
InputStream is = IOUtils.toInputStream(myString);
```
