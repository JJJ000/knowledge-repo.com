---
title: What is the syntax for printing a colored message using system.out.println?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use ANSI escape codes to print color in the console using System.out.println in Java.
---

**Contents**

[TOC]

### Color Codes

The following color codes can be used to print color in the console using System.out.println in Java:

- Black: `\u001B[30m`
- Red: `\u001B[31m`
- Green: `\u001B[32m`
- Yellow: `\u001B[33m`
- Blue: `\u001B[34m`
- Magenta: `\u001B[35m`
- Cyan: `\u001B[36m`
- White: `\u001B[37m`

### Usage

To use these color codes, simply add the appropriate code to the beginning of the System.out.println statement. For example:

```
System.out.println("\u001B[31mThis text will be printed in red!");
```

### Resetting the Color

It is important to remember to reset the color back to the default after printing in color. This can be done by adding the following code to the end of the statement:

`\u001B[0m`

### Example

The following example demonstrates how to print text in color and then reset the color back to the default:

```
System.out.println("\u001B[31mThis text will be printed in red!\u001B[0m");
```
