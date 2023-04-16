---
title: Mockito insert genuine objects into private @autowired fields
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Mockito can be used to inject real objects into private @Autowired fields in Java.
---

**Contents**

[TOC]

### Using Reflection

Reflection is a powerful tool that can be used to inject real objects into private @Autowired fields in Java. The following example shows how to use reflection to inject a real object into a private field:

```
// Get the private field
Field field = MyClass.class.getDeclaredField("myPrivateField");

// Make the field accessible
field.setAccessible(true);

// Create the real object
MyObject realObject = new MyObject();

// Inject the real object into the private field
field.set(myClassInstance, realObject);
```

### Using Mockito

Mockito is a popular Java mocking framework that can be used to inject real objects into private @Autowired fields. The following example shows how to use Mockito to inject a real object into a private field:

```
// Create the real object
MyObject realObject = new MyObject();

// Inject the real object into the private field
Mockito.when(myClassInstance.getMyPrivateField()).thenReturn(realObject);
```

### Using Constructors

Constructors can also be used to inject real objects into private @Autowired fields. The following example shows how to use a constructor to inject a real object into a private field:

```
// Create the real object
MyObject realObject = new MyObject();

// Create an instance of MyClass with the real object
MyClass myClassInstance = new MyClass(realObject);
```

### Using Setter Methods

Setter methods can also be used to inject real objects into private @Autowired fields. The following example shows how to use a setter method to inject a real object into a private field:

```
// Create the real object
MyObject realObject = new MyObject();

// Inject the real object into the private field
myClassInstance.setMyPrivateField(realObject);
```
