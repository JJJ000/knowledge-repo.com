---
title: Retrieving the constructor of an anonymous class
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Anonymous classes cannot be accessed directly, but their constructors can be accessed through a reference to the anonymous class instance.
---

**Contents**

[TOC]

#### Section 1: What is an Anonymous Class?
An anonymous class is a type of inner class in Java that does not have a name or identifier. It is declared and instantiated in a single statement and is used when a class is needed to be used only once.

#### Section 2: How to Access Constructor of an Anonymous Class?
The constructor of an anonymous class can be accessed by using the new keyword followed by the class definition. This will create an instance of the class and the constructor will be called automatically.

#### Section 3: Syntax
The syntax for accessing the constructor of an anonymous class is as follows: 
```
new <ClassName>() { 
    // class definition 
}
```

#### Section 4: Example
For example, if you want to access the constructor of an anonymous class named MyClass, the syntax would be as follows: 
```
MyClass obj = new MyClass() { 
    // class definition 
};
```
