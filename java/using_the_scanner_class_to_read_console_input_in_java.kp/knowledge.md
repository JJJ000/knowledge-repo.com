---
title: What is the syntax for using the scanner class to read input from the console in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can read input from the console using the Scanner class in Java by calling the Scanner object`s nextLine() or next() method.
---

**Contents**

[TOC]

# Section 1: Import the Scanner class

In order to use the Scanner class, you need to import the java.util.Scanner package. This can be done by adding the following line of code at the top of your program:

```java
import java.util.Scanner;
```

# Section 2: Create a Scanner object

Once the Scanner class is imported, you can create a Scanner object by passing the System.in object as an argument to the Scanner constructor. This will allow the Scanner object to read input from the console.

```java
Scanner scanner = new Scanner(System.in);
```

# Section 3: Read input from the console

Once the Scanner object is created, you can use the various methods available in the Scanner class to read input from the console. For example, the nextLine() method can be used to read a line of text from the console.

```java
String line = scanner.nextLine();
```

# Section 4: Close the Scanner object

Finally, it is important to close the Scanner object once you are done reading input from the console. This can be done by calling the close() method on the Scanner object.

```java
scanner.close();
```
