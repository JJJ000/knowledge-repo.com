---
title: Does JavaScript have a statement similar to the Python pass statement that performs no action?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Yes, in JavaScript the closest equivalent of Python`s pass statement that does nothing is an empty block statement, which is denoted by a pair of curly braces with nothing in between them.
---

**Contents**

[TOC]

Answer:

Yes, there is a JavaScript equivalent of the Python pass statement. However, it is not exactly the same. 

Section 1: The pass statement in Python
In Python, the pass statement is used when a statement is required syntactically but you don’t want to execute any code or do anything. For example, if you are defining a function or class and you haven’t yet implemented the functionality, you can use the pass statement to temporarily avoid the error that would occur if you left the code block empty. 

Here’s an example:

```
def some_function():
    pass
```

Section 2: The empty statement in JavaScript
In JavaScript, the closest equivalent to the pass statement in Python is the empty statement, which is simply a semicolon with nothing before it. 

Here’s an example:

```
function someFunction() {
    ;
}
```

Section 3: Limitations of the empty statement in JavaScript
However, it’s worth noting that the empty statement in JavaScript is not the same as the pass statement in Python. In Python, the pass statement explicitly does nothing, whereas in JavaScript, the empty statement simply does nothing because there is no code before the semicolon. 

If you use the empty statement to avoid syntax errors in a function or class definition, you must remember to come back and add the functionality later. 

Here’s an example:

```
function someFunction() {
    // TODO: Implement functionality later
    ;
}
```

Section 4: Conclusion
In conclusion, while there is a JavaScript equivalent of the Python pass statement in the form of the empty statement, it’s not exactly the same. The empty statement simply does nothing because there is no code before the semicolon. If you want to explicitly do nothing, you have to comment or document that intention instead.
