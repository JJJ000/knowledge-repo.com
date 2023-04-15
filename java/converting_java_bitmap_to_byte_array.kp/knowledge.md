---
title: Transforming a Java bitmap into a byte array
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Java Bitmap can be converted to a byte array by using the getPixels() method.
---

**Contents**

[TOC]

### Step 1: Convert Bitmap to Byte Array

```java
ByteArrayOutputStream stream = new ByteArrayOutputStream();
bitmap.compress(Bitmap.CompressFormat.PNG, 100, stream);
byte[] byteArray = stream.toByteArray();
```

### Step 2: Encode Byte Array to Base64

```java
String encodedImage = Base64.encodeToString(byteArray, Base64.DEFAULT);
```

### Step 3: Decode Base64 to Byte Array

```java
byte[] decodedString = Base64.decode(encodedImage, Base64.DEFAULT);
```

### Step 4: Convert Byte Array to Bitmap

```java
Bitmap decodedByte = BitmapFactory.decodeByteArray(decodedString, 0, decodedString.length);
```
