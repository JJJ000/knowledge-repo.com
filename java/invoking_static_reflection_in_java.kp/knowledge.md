---
title: Calling a static method using reflection
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To invoke a static method using reflection in Java, use the Method.invoke() method with the null parameter for the object instance.
---

**Contents**

[TOC]

### Step 1: Get the Class Object

To invoke a static method using reflection, first we need to get the Class object of the class whose static method we want to invoke. This can be done using the `Class.forName()` method:

```java
Class<?> cls = Class.forName("com.example.MyClass");
```

### Step 2: Get the Method

Once we have the Class object, we can use the `getDeclaredMethod()` method to get the method from the class:

```java
Method method = cls.getDeclaredMethod("myStaticMethod", int.class, String.class);
```

### Step 3: Invoke the Method

Finally, we can use the `invoke()` method to invoke the method:

```java
Object result = method.invoke(null, 1, "someString");
```

The first argument to the `invoke()` method is the object instance on which the method is to be invoked. Since the method is static, we can pass `null` as the first argument. The remaining arguments are the parameters to the method.
