---
title: How can I display a number between 0 and 9 with two digits?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use String.format(`%02d`, number) to format a number 0..9 to display with 2 digits.
---

**Contents**

[TOC]

1. Using `String.format`
--------------------------------
The `String.format` method can be used to format a number to display with two digits.

Syntax: `String.format("%02d", number);`

Example: 
```
int number = 5;
String formattedNumber = String.format("%02d", number);
System.out.println(formattedNumber); // output: 05
```

2. Using `DecimalFormat`
--------------------------------
The `DecimalFormat` class can also be used to format a number to display with two digits.

Syntax: `DecimalFormat df = new DecimalFormat("00");`

Example: 
```
int number = 5;
DecimalFormat df = new DecimalFormat("00");
String formattedNumber = df.format(number);
System.out.println(formattedNumber); // output: 05
```

3. Using `NumberFormat`
--------------------------------
The `NumberFormat` class can also be used to format a number to display with two digits.

Syntax: `NumberFormat nf = NumberFormat.getInstance(); nf.setMinimumIntegerDigits(2);`

Example: 
```
int number = 5;
NumberFormat nf = NumberFormat.getInstance();
nf.setMinimumIntegerDigits(2);
String formattedNumber = nf.format(number);
System.out.println(formattedNumber); // output: 05
```

4. Using `String.format` with `String.valueOf`
--------------------------------
The `String.format` method can also be used in conjunction with `String.valueOf` to format a number to display with two digits.

Syntax: `String.format("%02d", Integer.valueOf(number));`

Example: 
```
int number = 5;
String formattedNumber = String.format("%02d", Integer.valueOf(number));
System.out.println(formattedNumber); // output: 05
```
