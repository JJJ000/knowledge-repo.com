---
title: What are alternatives to using a switch statement in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Python does not have a switch statement, but it can be replaced with if-elif-else statements.
---

**Contents**

[TOC]

1. If-Else Statements 

If-else statements are a great alternative to switch statements in Python. They are more flexible and can be used to test multiple conditions at once. An if-else statement is structured as follows: 

```
if condition1:
    statement1
elif condition2:
    statement2
else:
    statement3
```

2. Dictionary Mapping 

Another way to replace switch statements in Python is to use a dictionary mapping. This involves creating a dictionary that maps each possible input to its corresponding output. The syntax for this is as follows: 

```
def switch_example(argument):
    switcher = {
        0: "zero",
        1: "one",
        2: "two",
    }
    return switcher.get(argument, "nothing")
```

3. Lambda Functions 

Lambda functions are another way to replace switch statements in Python. Lambda functions are anonymous functions that can be used to quickly define a function in a single line of code. The syntax for this is as follows: 

```
switch_example = lambda argument: "zero" if argument == 0 else "one" if argument == 1 else "two" if argument == 2 else "nothing"
```

4. Classes 

Classes are a powerful way to replace switch statements in Python. A class can be used to create a custom object that can be used to store data and define methods. The syntax for this is as follows: 

```
class SwitchExample:
    def __init__(self, argument):
        self.argument = argument

    def switch_example(self):
        if self.argument == 0:
            return "zero"
        elif self.argument == 1:
            return "one"
        elif self.argument == 2:
            return "two"
        else:
            return "nothing"
```
