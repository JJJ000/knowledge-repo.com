---
title: What is the process for obtaining user input in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To get user input in Java, use the Scanner class to read user input from the console.
---

**Contents**

[TOC]

1. Using `Scanner` Class
---------------------------------
The `Scanner` class is used to get user input, and it is found in the `java.util` package.

```java
import java.util.Scanner;

public class UserInput {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Your name is: " + name);
    }
}
```

2. Using `BufferedReader` Class
---------------------------------
The `BufferedReader` class is also used to get user input, and it is found in the `java.io` package.

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class UserInput {

    public static void main(String[] args) throws Exception {
        BufferedReader reader = 
            new BufferedReader(new InputStreamReader(System.in));
        System.out.println("Enter your name: ");
        String name = reader.readLine();
        System.out.println("Your name is: " + name);
    }
}
```

3. Using `Console` Class
---------------------------------
The `Console` class is also used to get user input, and it is found in the `java.io` package.

```java
import java.io.Console;

public class UserInput {

    public static void main(String[] args) {
        Console console = System.console();
        System.out.println("Enter your name: ");
        String name = console.readLine();
        System.out.println("Your name is: " + name);
    }
}
```

4. Using `JOptionPane` Class
---------------------------------
The `JOptionPane` class is also used to get user input, and it is found in the `javax.swing` package.

```java
import javax.swing.JOptionPane;

public class UserInput {

    public static void main(String[] args) {
        String name = JOptionPane.showInputDialog("Enter your name: ");
        System.out.println("Your name is: " + name);
    }
}
```
