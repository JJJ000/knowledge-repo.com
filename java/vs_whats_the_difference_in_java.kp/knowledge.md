---
title: What is the distinction between using || and |? why do we usually prefer one over the other?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The double pipe (||) is used to denote a logical OR operator, while the single pipe (|) is used to denote a bitwise OR operator in Java.
---

**Contents**

[TOC]

#Logical OR Operator
The logical OR operator (||) is used to perform a logical OR operation on two boolean expressions. It returns true if either one of the expressions is true, else it returns false.

#Bitwise OR Operator
The bitwise OR operator (|) is used to perform a bitwise OR operation on two expressions. It returns a 1 in each bit position for which the corresponding bits of either or both operands are 1s.

#Difference Between || and | in Java
The main difference between the logical OR operator (||) and the bitwise OR operator (|) in Java is that the logical OR operator (||) evaluates the second expression only if the first expression is false, while the bitwise OR operator (|) evaluates both the expressions regardless of the evaluation of the first expression.
