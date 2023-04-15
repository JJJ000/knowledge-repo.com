---
title: Convert a Java serializable object into a byte array
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: An object can be converted to a byte array by serializing it using the ObjectOutputStream class.
---

**Contents**

[TOC]

### Section 1 - Serializing the Object

To serialize an object to a byte array, you must first create an instance of a `java.io.ByteArrayOutputStream` object. Then, create an instance of a `java.io.ObjectOutputStream` object, passing the `ByteArrayOutputStream` object as a parameter. Finally, call the `writeObject()` method on the `ObjectOutputStream` instance, passing the object to be serialized as a parameter. This will serialize the object and write the serialized data to the `ByteArrayOutputStream`.

### Section 2 - Retrieving the Byte Array

Once the object has been serialized, the byte array can be retrieved by calling the `toByteArray()` method on the `ByteArrayOutputStream` instance. This will return the serialized data as a byte array.

### Section 3 - Closing Streams

Once the byte array has been retrieved, it is important to close the `ObjectOutputStream` and `ByteArrayOutputStream` objects to ensure that any resources associated with the streams are released. This can be done by calling the `close()` method on the stream objects.

### Section 4 - Example Code

The following example code demonstrates how to serialize an object to a byte array:

```java
Object objectToSerialize = ...;

ByteArrayOutputStream byteArrayOutputStream = new ByteArrayOutputStream();
ObjectOutputStream objectOutputStream = new ObjectOutputStream(byteArrayOutputStream);

objectOutputStream.writeObject(objectToSerialize);

byte[] serializedObject = byteArrayOutputStream.toByteArray();

objectOutputStream.close();
byteArrayOutputStream.close();
```
