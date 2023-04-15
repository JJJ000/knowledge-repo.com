---
title: What does __name__ == "__main__" do?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: It tells the program to execute the code inside the if statement only if the file is being run as the main program, not when it is being imported as a module.
---

**Contents**

[TOC]

### What is `__name__`

`__name__` is a special variable in Python. It is automatically set to "__main__" when a program is executed directly. When a program is imported, the `__name__` variable is set to the name of the module that is imported.

### What does `if __name__ == "__main__":` do?

The `if __name__ == "__main__"` statement is used to execute some code only if the file is run directly. It is usually used to run a set of test code or to provide a convenient user interface to a module.

### Example

```python
def main():
    print("Hello World!")

if __name__ == "__main__":
    main()
```

In the example above, the function main() will only be called if the file is run directly. If the file is imported into another program, the function main() will not be called.
