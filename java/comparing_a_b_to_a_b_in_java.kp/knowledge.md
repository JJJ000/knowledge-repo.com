---
title: What is the distinction between if (a - b < 0) and if (a < b)?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The difference between if (a - b < 0) and if (a < b) in Java is that the first statement evaluates if the difference between two values is less than 0, while the second statement evaluates if one value is less than the other.
---

**Contents**

[TOC]

## Syntax
The syntax of the two if statements are different: 

**If (a - b < 0)**
```
if (a - b < 0) {
    // code to execute
}
```

**If (a < b)**
```
if (a < b) {
    // code to execute
}
```

## Comparison
The two if statements have different meanings. 

**If (a - b < 0)**
This statement checks if the difference between the two variables is less than 0. 

**If (a < b)**
This statement checks if the value of the first variable is less than the value of the second variable. 

## Usage
The two if statements should be used in different scenarios. 

**If (a - b < 0)**
This statement should be used when you want to check if the difference between two variables is less than 0. 

**If (a < b)**
This statement should be used when you want to check if the value of the first variable is less than the value of the second variable.
