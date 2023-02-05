---
title: Retrieving the parent class instance from the nested class instance
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The outer class object can be obtained from the inner class object by calling the getOuter() method on the inner class object.
---

**Contents**

[TOC]

**Section 1: Definition of Outer and Inner Classes**

In Java, classes can be nested within other classes, allowing for a hierarchical structure of objects. The class that is nested within another class is referred to as an inner class, while the class that contains the inner class is referred to as the outer class.

**Section 2: Accessing Outer Class from Inner Class**

An inner class can access the members of its outer class, including private members. This is done by using the keyword “this” to refer to the outer class. For example: 

```
class OuterClass {
    private int x;
    class InnerClass {
        void accessOuterClass() {
            x = 10;
        }
    }
}
```

**Section 3: Getting Hold of Outer Class Object**

In order to get a hold of the outer class object from the inner class object, the inner class object must first be instantiated. Then, the outer class object can be accessed using the “getOuterClass()” method. For example: 

```
OuterClass outerClass = new OuterClass();
OuterClass.InnerClass innerClass = outerClass.new InnerClass();
innerClass.accessOuterClass();
OuterClass outerClassObject = innerClass.getOuterClass();
```

**Section 4: Conclusion**

In conclusion, it is possible to get a hold of the outer class object from the inner class object in Java by instantiating the inner class object and then using the “getOuterClass()” method to access the outer class object.
