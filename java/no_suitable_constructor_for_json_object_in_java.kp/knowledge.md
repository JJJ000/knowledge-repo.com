---
title: No appropriate constructor was found for the specified type [simple type, class] it is not possible to create an instance from a JSON object
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A no-arg constructor must be provided for the class in order to instantiate it from a JSON object.
---

**Contents**

[TOC]

### Overview
A JsonMappingException is an exception thrown by Jackson when it fails to map a JSON object to a Java object. This exception is thrown when Jackson fails to find a suitable constructor for the type specified.

### Causes
This exception is usually caused by the absence of a suitable constructor in the target Java class. The constructor must be able to accept the fields of the JSON object as parameters. If the constructor is not present, or if the parameters do not match the fields of the JSON object, then Jackson will be unable to instantiate the Java object from the JSON object.

### Solutions
The solution to this problem is to ensure that the target Java class has a suitable constructor. The constructor must accept the fields of the JSON object as parameters. If the constructor does not exist, it must be added to the class. If the parameters of the constructor do not match the fields of the JSON object, then the parameters must be adjusted to match the fields.

### Conclusion
In conclusion, a JsonMappingException is thrown when Jackson is unable to instantiate a Java object from a JSON object due to the absence of a suitable constructor. The solution to this problem is to ensure that the target Java class has a suitable constructor with parameters that match the fields of the JSON object.
