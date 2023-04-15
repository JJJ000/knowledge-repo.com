---
title: What is the process for transforming an inputstream into a string in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the InputStreamReader and BufferedReader classes to read the InputStream into a String.
---

**Contents**

[TOC]

### Creating a BufferedReader
The first step in reading an InputStream into a String is to create a BufferedReader from the InputStream. This can be done using the following code:

```java
BufferedReader reader = new BufferedReader(new InputStreamReader(inputStream));
```

### Reading the InputStream
The next step is to read the InputStream using the BufferedReader. This can be done using the readLine() method of the BufferedReader. This will return a String which can be used to build the resulting String.

### Building the String
The resulting String can be built using the StringBuilder class. The readLine() method of the BufferedReader can be used in a loop to append each line of the InputStream to the StringBuilder.

### Returning the String
Once the String has been built, the toString() method of the StringBuilder class can be used to return the resulting String.
