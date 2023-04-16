---
title: How can I obtain a class literal from a generic type in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the syntax Class<T>.class to get a class literal from a generic type T.
---

**Contents**

[TOC]

1. Introduction
2. Using Class.forName()
3. Using the Class.getClass() Method
4. Conclusion

## Introduction
A class literal is a reference to a class, which is often used when working with Java generics. It is a way of referencing a class without having to create an instance of it. In Java, there are two ways of getting a class literal from a generic type: using the Class.forName() method or using the Class.getClass() method. 

## Using Class.forName()
The Class.forName() method is a static method that takes a String parameter representing the fully-qualified name of the class and returns a Class object representing the class. This method can be used to get a class literal from a generic type. 

For example, if we wanted to get a class literal for the generic type String, we could use the following code: 

```
Class<String> stringClass = (Class<String>) Class.forName("java.lang.String");
```

## Using the Class.getClass() Method
The Class.getClass() method is a non-static method that takes no parameters and returns a Class object representing the class. This method can also be used to get a class literal from a generic type. 

For example, if we wanted to get a class literal for the generic type String, we could use the following code: 

```
Class<String> stringClass = (Class<String>) "Hello".getClass();
```

## Conclusion
In Java, there are two ways of getting a class literal from a generic type: using the Class.forName() method or using the Class.getClass() method. Both of these methods can be used to get a class literal from a generic type, but the Class.forName() method requires a String parameter representing the fully-qualified name of the class while the Class.getClass() method takes no parameters.
