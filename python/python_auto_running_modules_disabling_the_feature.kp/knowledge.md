---
title: How can I prevent Python from executing my module upon import?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Python runs the code in the module when it`s imported, to prevent this use a conditional statement at the bottom of the module.
---

**Contents**

[TOC]

Section 1: Python module loading process

When you import a module in Python, the interpreter looks for the module and loads it into memory. During this process, it evaluates the module code and executes any top-level statements, including function and class definitions.

Section 2: The __name__ variable

When Python executes a module, it sets the __name__ variable to a special value depending on how the module was executed. If the module is the main program, __name__ is set to "__main__". If the module is being imported, __name__ is set to the name of the module.

Section 3: Conditional module execution

You can use the __name__ variable to prevent a module from executing when it is imported. To do this, you can place the code you want to execute only when the module is run as the main program inside a conditional block that checks if __name__ equals "__main__". For example:

```
def some_function():
    print("This function will only execute if the module is run as the main program")

if __name__ == "__main__":
    some_function()
```

Section 4: Conclusion

In conclusion, Python executes the code in a module when it is imported. To prevent a module from executing when it is imported, you can use the __name__ variable to conditionally execute code when the module is run as the main program.
