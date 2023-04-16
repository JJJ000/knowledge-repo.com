---
title: Declaring multiple classes in a single Java file
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, multiple class declarations can be included in one file in Java, as long as only one of the classes is declared public.
---

**Contents**

[TOC]

#Yes

##Syntax

Multiple class declarations in one file is allowed in Java. The syntax for declaring multiple classes in one file is as follows:

```
public class ClassName1 {
    // class body
}

public class ClassName2 {
    // class body
}
```

##Restrictions

When declaring multiple classes in one file, there are a few restrictions to consider:

- Only one public class is allowed in the file and it must have the same name as the file.
- All other classes must be declared with the default (package-private) access modifier.
- The file must be saved with the name of the public class.

##Example

For example, the following code declares two classes in one file:

```
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}

class Foo {
    public void doSomething() {
        System.out.println("Doing something...");
    }
}
```

The file must be saved as `Main.java` and the class `Foo` must be declared with the default (package-private) access modifier.
