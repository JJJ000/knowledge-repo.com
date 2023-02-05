---
title: Do private fields get passed down to subclasses?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, private fields are not inherited by subclasses in Java.
---

**Contents**

[TOC]

#No

##Explanation
Private fields are not inherited in Java. Private fields are only accessible within the class in which they are declared. Subclasses do not have access to the private fields of their superclasses, even if they are declared in the same package.

##Example
For example, consider the following code: 

```
class SuperClass {
    private int x;
}

class SubClass extends SuperClass {
    public void printX() {
        System.out.println(x);
    }
}
```

In this example, the `SubClass` does not have access to the `x` field of the `SuperClass`. As such, the `printX()` method will not compile, since it is attempting to access a private field.

##Conclusion
In conclusion, subclasses do not inherit private fields in Java.
