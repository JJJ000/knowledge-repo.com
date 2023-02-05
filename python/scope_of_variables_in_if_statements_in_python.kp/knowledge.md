---
title: What is the range of a variable declared within an if statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The scope of a variable initialized in an if statement in Python is limited to the block of code in which it is declared.
---

**Contents**

[TOC]

# Local Scope
A variable initialized in an if statement in Python will only be accessible within the code block of the if statement. It will not be accessible outside of the if statement. 

# Global Scope 
If the variable is initialized outside of the if statement, it will have global scope, meaning that it can be accessed from anywhere in the program. 

# Nested Scope
If the if statement is nested within another code block, the variable will only be accessible within the scope of the nested code block. 

# Closure Scope
A variable initialized in an if statement can be accessed in a closure, i.e. a function defined within the scope of the if statement. The variable will not be accessible outside of the closure.
