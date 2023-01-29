---
title: What is the best way to turn a stack trace into a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the printStackTrace() method of the Throwable class to convert a stack trace to a string.
---

**Contents**

[TOC]

### 1. Using PrintWriter

PrintWriter is a class in Java that allows for the writing of formatted data to an output stream. It can be used to convert a stack trace to a string.

1. Create a PrintWriter object and pass a StringWriter object as an argument.

```java
StringWriter sw = new StringWriter();
PrintWriter pw = new PrintWriter(sw);
```

2. Pass the Throwable object to the PrintWriter's printStackTrace() method.

```java
try {
    throw new Exception("Test Exception");
} catch (Exception e) {
    e.printStackTrace(pw);
}
```

3. Call the toString() method on the StringWriter object.

```java
String stackTraceString = sw.toString();
```

### 2. Using StringWriter

StringWriter is a class in Java that allows for the writing of character data to a string buffer. It can also be used to convert a stack trace to a string.

1. Create a StringWriter object.

```java
StringWriter sw = new StringWriter();
```

2. Pass the Throwable object to the StringWriter's printStackTrace() method.

```java
try {
    throw new Exception("Test Exception");
} catch (Exception e) {
    e.printStackTrace(sw);
}
```

3. Call the toString() method on the StringWriter object.

```java
String stackTraceString = sw.toString();
```
