---
title: What is the advantage of using (a*b != 0) instead of (a != 0 && b != 0) in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Because (a*b != 0) only requires one comparison, while (a != 0 && b != 0) requires two comparisons.
---

**Contents**

[TOC]

### Explanation

When evaluating expressions, Java takes a bottom-up approach. This means that it evaluates the expressions inside the parentheses first, and then applies the operator outside the parentheses. 

### a*b != 0
In this case, the expression inside the parentheses is `a*b`, which is evaluated first. If the result is non-zero, the expression evaluates to `true`. 

### a != 0 && b != 0
In this case, the expression inside the parentheses is `a != 0` and `b != 0`. Both of these expressions must be evaluated first, before the `&&` operator can be applied. This means that the expression takes longer to evaluate than the first one. 

### Conclusion
Therefore, the expression `a*b != 0` is faster than `a != 0 && b != 0` because it requires fewer steps to evaluate.
