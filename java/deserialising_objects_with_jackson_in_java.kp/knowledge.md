---
title: What is the process of deserialising an array of objects using jackson?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the ObjectMapper.readValue() method to deserialize an array of objects in Java using Jackson.
---

**Contents**

[TOC]

### Initial Setup

To use Jackson to deserialise an array of objects in Java, the following steps should be taken:

1. Add the Jackson dependency to the project.
2. Create a Java class for the serialised object, with the appropriate fields and getters/setters.
3. Create a Java class for the array of objects, with a field of the type of the serialised object.
4. Create a Jackson ObjectMapper instance.

### Deserialising the Array

Once the initial setup is complete, deserialising the array of objects is relatively straightforward. The following steps should be taken:

1. Read the JSON string into a Java String object.
2. Use the ObjectMapper instance to deserialise the JSON string into an array of the serialised object.
3. Iterate through the array and access the individual objects.

### Error Handling

In the event of an error during deserialisation, the ObjectMapper instance will throw an exception. Therefore, it is important to handle errors appropriately. The following steps should be taken:

1. Wrap the deserialisation code in a try/catch block.
2. Catch the appropriate exception (e.g. JsonParseException).
3. Handle the error appropriately (e.g. log the error and return an appropriate error message).

### Conclusion

Using Jackson to deserialise an array of objects in Java is relatively straightforward. By following the steps outlined in this answer, developers should be able to successfully deserialise an array of objects.
