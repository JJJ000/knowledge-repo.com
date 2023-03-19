---
title: What are the steps for providing arguments to a button command in tkinter?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can pass arguments to a Button command in Tkinter by using lambda or partial functions.
---

**Contents**

[TOC]

# Introduction

Buttons in Tkinter provide a simple way to trigger actions when pressed. By default, they execute a command function that is predefined when creating the button. However, in many cases, we may want the command function to take arguments based on user inputs or other conditions. In this guide, we will explore how to pass arguments to a button command in Tkinter in Python.

# Using a lambda function

One way to pass arguments to a button command is to use a lambda function. A lambda function is an anonymous function that can take arguments and return a value. Here is an example of how to use a lambda function to pass an argument to a button command:

```
import tkinter as tk

root = tk.Tk()

def greet(name):
    print(f"Hello, {name}!")

btn = tk.Button(root, text="Say hello", command=lambda: greet("John"))
btn.pack()

root.mainloop()
```

In this example, we created a button with the text "Say hello". We set its command attribute to a lambda function that calls the greet function with the argument "John". When the button is pressed, it will execute the lambda function, which in turn calls the greet function with the argument "John". The output will be "Hello, John!" in the console.

# Using a partial function

Another way to pass arguments to a button command is to use a partial function. A partial function is a function that is derived from an existing function by fixing some of its arguments. Here is an example of how to use a partial function to pass an argument to a button command:

```
import tkinter as tk
from functools import partial

root = tk.Tk()

def greet(greeting, name):
    print(f"{greeting}, {name}!")

greet_hello = partial(greet, "Hello")
greet_hi = partial(greet, "Hi")

btn_hello = tk.Button(root, text="Say hello", command=greet_hello("John"))
btn_hi = tk.Button(root, text="Say hi", command=greet_hi("Alice"))

btn_hello.pack()
btn_hi.pack()

root.mainloop()
```

In this example, we created a greet function that takes two arguments: a greeting and a name. We used the partial function from the functools module to create two new functions: greet_hello and greet_hi. The greet_hello function is a partial function of greet with the first argument fixed to "Hello", while the greet_hi function is a partial function of greet with the first argument fixed to "Hi". We then created two buttons with the text "Say hello" and "Say hi", respectively. We set their command attribute to greet_hello("John") and greet_hi("Alice"), respectively, which are both functions that take one argument and call the greet function with the fixed greeting and the name argument provided. When the buttons are pressed, they will execute the corresponding functions, which in turn call the greet function with the appropriate arguments. The output will be "Hello, John!" or "Hi, Alice!" in the console.

# Using the bind method

A third way to pass arguments to a button command is to use the bind method. The bind method allows us to bind a function to an event, such as the "Button-1" event that occurs when the left mouse button is clicked on a widget. Here is an example of how to use the bind method to pass an argument to a button command:

```
import tkinter as tk

root = tk.Tk()

def greet(event, name):
    print(f"Hello, {name}!")

btn = tk.Button(root, text="Say hello")
btn.pack()
btn.bind("<Button-1>", lambda event: greet(event, "John"))

root.mainloop()
```

In this example, we created a button with the text "Say hello". We did not set its command attribute. Instead, we used the bind method to bind the greet function to the "Button-1" event that occurs when the left mouse button is clicked on the button widget. We passed a lambda function that calls the greet function with the argument "John" as the second argument to the bind method. When the button is clicked, it will execute the lambda function, which in turn calls the greet function with the event object and the argument "John". The output will be "Hello, John!" in the console.

# Conclusion

We have explored three different ways to pass arguments to a button command in Tkinter in Python: using a lambda function, using a partial function, and using the bind method. Each method has its own advantages and disadvantages, depending on the specific use case. By using these techniques, we can create more dynamic and interactive GUI applications.
