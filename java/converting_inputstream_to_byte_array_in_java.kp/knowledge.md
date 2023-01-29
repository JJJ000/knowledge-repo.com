---
title: Change an inputstream into a byte array in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The InputStream can be converted to a byte array by using the read() method of the InputStream class.
---

**Contents**

[TOC]

### Overview
Java provides multiple ways to convert an InputStream to a byte array. Depending on the size of the InputStream, the most efficient approach may vary.

### Using ByteArrayOutputStream
One approach is to use a `ByteArrayOutputStream` to copy the contents of the InputStream.

```java
// Create a ByteArrayOutputStream
ByteArrayOutputStream bos = new ByteArrayOutputStream();

// Read the InputStream and write it to the ByteArrayOutputStream
byte[] buffer = new byte[1024];
int len;
while ((len = inputStream.read(buffer)) > -1) {
    bos.write(buffer, 0, len);
}

// Convert the ByteArrayOutputStream to a byte array
byte[] result = bos.toByteArray();
```

### Using Apache Commons IO
Another approach is to use the `IOUtils` class from the Apache Commons IO library.

```java
// Use the IOUtils class from Apache Commons IO to convert the InputStream to a byte array
byte[] result = IOUtils.toByteArray(inputStream);
```

### Conclusion
Both approaches provide a way to convert an InputStream to a byte array in Java. Depending on the size of the InputStream, one approach may be more efficient than the other.
