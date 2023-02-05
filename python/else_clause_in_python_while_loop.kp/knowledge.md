---
title: The 'else' statement in a Python 'while' loop
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The else clause is executed when the condition in the while statement is no longer true, and it is optional.
---

**Contents**

[TOC]

### Syntax
The syntax of an else clause on a while statement in Python is as follows:

```
while condition:
    statements
else:
    statements
```

### Functionality
The else clause is executed when the while loop terminates normally (i.e. when the condition becomes false). This means that the else clause is not executed if the loop is terminated by a break statement.

### Example
Here is an example of a while loop with an else clause:

```
i = 0
while i < 10:
    print(i)
    i += 1
else:
    print("Loop terminated normally")
```

### Output
This code will print the numbers 0 to 9, and then the message "Loop terminated normally".
