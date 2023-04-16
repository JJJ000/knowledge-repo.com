---
title: What is the process for creating an inputstreamreader from a string in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the constructor InputStreamReader(String s) to create an InputStreamReader from a String.
---

**Contents**

[TOC]

### Option 1: Using ByteArrayInputStream

1. Create a byte array from the String: 

```java
byte[] byteArray = string.getBytes();
```

2. Create a ByteArrayInputStream from the byte array:

```java
ByteArrayInputStream byteArrayInputStream = new ByteArrayInputStream(byteArray);
```

3. Create an InputStreamReader from the ByteArrayInputStream:

```java
InputStreamReader inputStreamReader = new InputStreamReader(byteArrayInputStream);
```

### Option 2: Using StringReader

1. Create a StringReader from the String:

```java
StringReader stringReader = new StringReader(string);
```

2. Create an InputStreamReader from the StringReader:

```java
InputStreamReader inputStreamReader = new InputStreamReader(stringReader);
```
