---
title: Testing system.out.println() using junit
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A JUnit test for System.out.println() in Java would involve asserting that the correct output was printed to the console.
---

**Contents**

[TOC]

### System.out.println()
System.out.println() is a Java statement that prints the argument passed, into the System.out which is generally a console. It works like the print() and println() methods of PrintStream class.

### Syntax
The syntax of the System.out.println() statement is given below:

System.out.println(Object obj);

### Example
For example, the following statement prints the string "Hello World!" on the console.

System.out.println("Hello World!");

### JUnit Test
The following is an example of a JUnit test for System.out.println():

import static org.junit.Assert.*;
import org.junit.Test;

public class SystemOutPrintlnTest {
    @Test
    public void testSystemOutPrintln() {
        String output = "Hello World!";
        System.out.println(output);
        assertEquals("Hello World!", output);
    }
}
