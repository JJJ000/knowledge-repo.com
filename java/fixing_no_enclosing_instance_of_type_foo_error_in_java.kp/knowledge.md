---
title: What is the source of the "no enclosing instance of type foo is accessible" error, and how can it be resolved?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: This error occurs when a non-static method or field is referenced from a static context, and can be fixed by making the method or field static.
---

**Contents**

[TOC]

#Cause 
This error occurs when a non-static nested class, or inner class, attempts to access a field or method of an enclosing class without an instance of the enclosing class. 

#Example
For example, let's say we have a class Foo, and a non-static inner class Bar:

```java
public class Foo {
    public void someMethod() {
        System.out.println("Hello from Foo");
    }
    
    public class Bar {
        public void someOtherMethod() {
            System.out.println("Hello from Bar");
        }
    }
}
```

If we try to create an instance of Bar without an instance of Foo, we will get an error:

```java
Bar bar = new Bar();
```

This will result in the error "No enclosing instance of type Foo is accessible".

#Solution
The solution is to create an instance of the enclosing class before creating an instance of the inner class. For example:

```java
Foo foo = new Foo();
Bar bar = foo.new Bar();
```

This will create an instance of Foo and then an instance of Bar, which will allow us to access the fields and methods of Foo.
