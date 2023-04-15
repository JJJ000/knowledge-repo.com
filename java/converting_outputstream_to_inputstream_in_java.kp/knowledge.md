---
title: What is the process for transforming an outputstream into an inputstream?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the constructor of InputStream that takes an OutputStream as an argument.
---

**Contents**

[TOC]

### Overview

Java provides a number of ways to convert an OutputStream to an InputStream. Depending on the specific use case, different methods may be more suitable than others. 

### ByteArrayInputStream

One of the simplest approaches is to use a ByteArrayInputStream. This method creates an InputStream from an array of bytes. To use this approach, write the OutputStream to a byte array, then create an InputStream from the byte array.

### PipedInputStream

Another approach is to use a PipedInputStream. This method connects an OutputStream to an InputStream, allowing data to be written to the OutputStream and then read from the InputStream.

### BufferedInputStream

Finally, a BufferedInputStream can be used to wrap an OutputStream. This approach allows the OutputStream to be read from the InputStream as if it were a file.
