---
title: Converting to base64 in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Base64 encoding in Java can be achieved using the java.util.Base64 class.
---

**Contents**

[TOC]

### Overview
Base64 is an encoding scheme used to represent binary data in an ASCII string format. It is used to encode and decode data in order to protect it from modification or corruption.

### Encoding with Base64
Base64 encoding can be achieved in Java using the `java.util.Base64` class. This class provides three different encoders and decoders to encrypt information at each level.

The `Base64.Encoder` class provides methods to encode a byte array into a String using the Base64 encoding scheme. The `Base64.Decoder` class provides methods to decode a byte array from a String using the Base64 encoding scheme.

### Example
The following example demonstrates how to encode and decode a byte array using the Base64 encoding scheme in Java:

```java
import java.util.Base64;

public class Base64Example {
    public static void main(String[] args) {
        // Encode a byte array
        byte[] encodedBytes = Base64.getEncoder().encode("Hello World".getBytes());
        System.out.println(new String(encodedBytes));
        
        // Decode a byte array
        byte[] decodedBytes = Base64.getDecoder().decode(encodedBytes);
        System.out.println(new String(decodedBytes));
    }
}
```

The output of the above program is:

```
SGVsbG8gV29ybGQ=
Hello World
```

### Conclusion
Base64 encoding is a useful technique to protect data from corruption or modification. It can be easily implemented in Java using the `java.util.Base64` class.
