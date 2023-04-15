---
title: What is the purpose of the "static" keyword when used after "import"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `static` modifier after `import` in Java indicates that all of the members of the imported class are imported as static members.
---

**Contents**

[TOC]

### Definition

The static keyword after an import statement in Java is used to import the members of a class or interface as static members. This allows the imported members to be used without qualifying them with the class or interface name.

### Benefits 

Using the static keyword after an import statement provides several benefits. It allows the programmer to use the imported members directly without having to use the fully qualified class name. This makes the code more concise and readable. Additionally, it allows the programmer to access static members of the imported class without having to create an instance of the class.

### Example

For example, consider the following code: 

```java
import static java.lang.Math.*;

public class Test {
    public static void main(String[] args) {
        System.out.println(PI);
    }
}
```

In this example, the static keyword after the import statement allows the programmer to directly access the PI constant from the Math class without having to use the fully qualified class name (i.e. java.lang.Math.PI).

### Conclusion

The static keyword after an import statement in Java is used to import the members of a class or interface as static members. This allows the imported members to be used directly without having to qualify them with the class or interface name, making the code more concise and readable. Additionally, it allows the programmer to access static members of the imported class without having to create an instance of the class.
