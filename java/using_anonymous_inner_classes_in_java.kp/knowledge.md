---
title: What are the uses of anonymous inner classes in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Anonymous inner classes are used in Java to create an instance of a class without having to declare a named class.
---

**Contents**

[TOC]

### Definition
Anonymous inner classes are inner classes that are declared and instantiated in a single statement without giving the class a name.

### Benefits
Anonymous inner classes are useful when a class needs to be accessed only once. They are also useful when the class needs to override methods of the superclass or implement methods of an interface.

### Syntax
Anonymous inner classes are declared and instantiated using the following syntax:

```
new SuperClassOrInterface() {
    //body of the class
}
```

### Example
For example, a Runnable interface can be implemented using an anonymous inner class:

```
Runnable r = new Runnable() {
    public void run() {
        //code to be executed
    }
};
```
