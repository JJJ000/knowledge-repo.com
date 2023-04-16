---
title: What is the result of adding 1 to an empty array, then adding 1 to that result, then adding 1 to that result again?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The expression evaluates to the string `10` because the two arrays are coerced to numbers and then added together.
---

**Contents**

[TOC]

# Explanation
The expression `++[[]][+[]]+[+[]]` is a combination of two operators, the increment operator (`++`) and the addition operator (`+`). The increment operator is used to increment a value by one, while the addition operator is used to add two values together. 

# Arithmetic
In this expression, the increment operator is applied to the array `[[]][+[]]`, which is equivalent to `[[]]` since `+[]` evaluates to `0`. The increment operator then increments the value of the array by one, making it `[[1]]`. The addition operator is then applied to the result of the increment operator and `[+[]]`, which is equivalent to `[0]`. This adds the two values together, resulting in `[[1], 0]`.

# Evaluation
The expression is then evaluated as a string, which concatenates the two values together to form the string "10". This is because the array `[[1], 0]` is equivalent to `[1, 0]`, which when evaluated as a string results in "10". 

# Conclusion
Therefore, the expression `++[[]][+[]]+[+[]]` evaluates to the string "10" in Javascript.
