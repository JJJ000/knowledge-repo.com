---
title: Copying data from a Java inputstream to an outputstream in an easy manner
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The contents of an InputStream can be written to an OutputStream using the copy() method of the Apache Commons IO library.
---

**Contents**

[TOC]

### Initializing Streams

Before writing contents of an InputStream to an OutputStream, it is important to initialize the streams. To do this, first declare and instantiate the InputStream and OutputStream variables. 

InputStream inputStream = new FileInputStream(inputFile);
OutputStream outputStream = new FileOutputStream(outputFile);

### Writing to OutputStream

Once the streams are initialized, writing to the OutputStream is relatively straightforward. To do this, use the write() method of the OutputStream class. This method takes in a byte array as an argument and writes the contents of the array to the OutputStream. 

byte[] buffer = new byte[1024];
int length;
while((length = inputStream.read(buffer)) > 0) {
    outputStream.write(buffer, 0, length);
}

### Closing Streams

After writing the contents of the InputStream to the OutputStream, it is important to close the streams. This can be done by using the close() method of both the InputStream and OutputStream classes. 

inputStream.close();
outputStream.close();

### Flushing OutputStream

Finally, it is a good practice to flush the OutputStream after writing to it. This can be done by using the flush() method of the OutputStream class. 

outputStream.flush();
