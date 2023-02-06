---
title: Determine if a Java class object is a subclass of another class object
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, a Class Object can be a subclass of another Class Object in Java.
---

**Contents**

[TOC]

# Section 1: Check if a Class Object is Subclass

In Java, a class object can be checked to determine if it is a subclass of another class object. This can be done by using the `instanceof` operator. 

The `instanceof` operator is a binary operator that takes two operands: an object reference and a type. It returns a boolean value of true if the object reference is an instance of the specified type, or false otherwise.

# Section 2: Syntax

The syntax for using the `instanceof` operator is as follows:

```
objectReference instanceof Type
```

where `objectReference` is the object reference to be tested and `Type` is the type to be tested against.

# Section 3: Example

For example, if we have two classes, `SuperClass` and `SubClass`, where `SubClass` is a subclass of `SuperClass`, we can use the `instanceof` operator to check if an object of type `SubClass` is an instance of `SuperClass`:

```
SubClass obj = new SubClass();
if (obj instanceof SuperClass) {
    System.out.println("obj is an instance of SuperClass");
}
```

# Section 4: Output

The output of the above code would be:

```
obj is an instance of SuperClass
```
