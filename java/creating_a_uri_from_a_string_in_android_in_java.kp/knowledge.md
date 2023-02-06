---
title: Converting a string into a uri in android
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use Uri.parse(String) to turn a string into a Uri in Android in Java.
---

**Contents**

[TOC]

1. **Creating the Uri Object**

To turn a string into a Uri object in Android in Java, you can use the `Uri.parse()` method. This method takes a string as an argument and returns a Uri object.

For example: 

```java
String myString = "https://www.example.com";
Uri myUri = Uri.parse(myString);
```

2. **Using the Uri Object**

Once you have a Uri object, you can use it to access the components of the Uri. For example, you can use the `getScheme()` method to get the scheme (e.g. "https") of the Uri, and the `getHost()` method to get the host (e.g. "www.example.com").

For example: 

```java
String scheme = myUri.getScheme(); // "https"
String host = myUri.getHost(); // "www.example.com"
```

3. **Building a Uri**

You can also use the Uri object to build a Uri from components. For example, you can use the `Uri.Builder` class to construct a Uri from individual components.

For example:

```java
Uri.Builder builder = new Uri.Builder();
builder.scheme("https")
       .authority("www.example.com")
       .path("/mypath")
       .query("myquery");
Uri myUri = builder.build();
```

4. **Converting a Uri to a String**

Finally, you can convert a Uri object back to a string using the `Uri.toString()` method.

For example:

```java
String myString = myUri.toString(); // "https://www.example.com/mypath?myquery"
```
