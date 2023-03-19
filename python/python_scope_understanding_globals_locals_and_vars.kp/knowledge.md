---
title: Could you explain the distinction among globals(), locals(), and vars()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: globals() returns a dictionary of global symbols, locals() returns a dictionary of local symbols, and vars() returns the \_\_dict\_\_ attribute of an object or the current local symbol table when called with no argument; all three are used for introspection purposes.
---

**Contents**

[TOC]

# Introduction 

Python provides three built-in functions to retrieve the information about the variables in the program: globals(), locals(), and vars(). Despite their similarities in functionality, they differ in their scope and usage. In this article, we'll explore the similarities and differences between these three functions.

# globals() 

The globals() function returns a dictionary representing the global symbol table of the current module or namespace. It contains the names and values of all global variables defined in the current scope.

```python
x = "global variable"

def foo():
    y = "local variable"
    print(globals())
    
foo()
```

Output:
```
{'__name__': '__main__', '__doc__': None, '__package__': None, '__loader__': <class '_frozen_importlib.BuiltinImporter'>, '__spec__': None, '__annotations__': {}, '__builtins__': <module 'builtins' (built-in)>, 'x': 'global variable', 'foo': <function foo at 0x7f61ac9a39d0>}
```

In the above example, globals() function returns a dictionary that includes the names and values of all global variables defined in the current module.

# locals()

The locals() function returns a dictionary representing the current local symbol table. It contains the names and values of all local variables defined within the current scope.

```python
def foo():
    x = "local variable"
    print(locals())
    
foo()
```

Output:
```
{'x': 'local variable'}
```

In the above example, locals() function returns a dictionary that includes the names and values of all local variables defined within the foo() function.

# vars()

The vars() function is similar to the locals() function, but it takes an object as an argument and returns the dictionary representing the object's namespace.

```python
class MyClass:
    def __init__(self):
        self.x = "instance variable"
        
obj = MyClass()

print(vars(obj))
```

Output:
```
{'x': 'instance variable'}
```

In the above example, vars() function returns a dictionary that includes the names and values of all the instance variables defined within the obj object.

# Conclusion

In conclusion, globals(), locals(), and vars() are built-in functions to retrieve the information about the variables in Python. While globals() returns a dictionary representing the global symbol table of the current module or namespace, locals() returns a dictionary representing the current local symbol table. On the other hand, vars() takes an object as an argument and returns a dictionary representing the object's namespace.
