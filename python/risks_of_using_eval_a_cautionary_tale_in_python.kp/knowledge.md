---
title: What makes the use of 'eval' considered as a poor approach?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Using `eval` is considered a bad practice in Python because it can execute arbitrary code and potentially be exploited by attackers to inject malicious code.
---

**Contents**

[TOC]

## Introduction
`eval` is a built-in function in Python that is used for evaluating a string as a Python expression. While it can be useful in certain scenarios, using `eval` is generally considered a bad practice in Python. This answer will explore the reasons why.

## Security Risks
One of the main reasons why using `eval` is a bad practice in Python is because it can introduce security risks. When you use `eval` to execute a string as Python code, you are essentially giving control of your program to whoever wrote that string. If the string is provided by an untrusted source, it could contain code that could harm your system or steal your data. For instance, consider the following code:

```python
user_input = input("Enter a Python expression: ")
result = eval(user_input)
print(result)
```

If a user enters `"os.system('rm -rf /')"` as their input, the `eval` function will execute that code and delete all the files on your system!

## Performance Issues
Another reason why using `eval` is a bad practice in Python is because it can have significant performance issues. When you use `eval`, Python has to first parse the string into a Python expression, and then execute that expression. This can be much slower than simply executing Python code directly. In addition, because `eval` is a dynamic feature, it can make it harder for Python's interpreter to optimize your code for speed.

## Code Clarity
Finally, using `eval` can make your code harder to read, understand, and maintain. When you use `eval`, you are essentially writing code in strings, which can be harder to read and understand than code that is written directly in Python. This can make it difficult for others to understand your code, or for you to come back to your code later and remember what you were doing.

## Conclusion
Given these security, performance, and code clarity issues, it is generally recommended that Python developers avoid using `eval` whenever possible. While there are some situations where `eval` may be useful, such as in the context of a REPL or interactive shell, in most cases there are better and safer ways to achieve the same goals.
