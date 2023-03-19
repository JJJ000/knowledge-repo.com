---
title: What is the way to incorporate your own code with tkinter's event loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `after()` method to schedule the execution of your code after the main event loop has finished processing the current events.
---

**Contents**

[TOC]

# Running Own Code Alongside Tkinter's Event Loop in Python

There might be times when you want to run your own code in a Tkinter-based application without blocking the main event loop that handles user input and other actions. This can be achieved by properly structuring your code and using the appropriate Tkinter methods. Here are the steps to follow:

## Step 1 - Create a function for your code

Before integrating your code with Tkinter's event loop, you need to encapsulate it in a separate function that can be called from the main program. This function should accept parameters if necessary and return any relevant values. 

For example, say you want to periodically update a label with the current time. You can write a function to do this:

```python
import datetime

def update_label(label):
    current_time = datetime.datetime.now().strftime('%H:%M:%S')
    label.config(text=current_time)
```

This function takes a Tkinter label widget as an argument and updates its text with the current time formatted as 'hh:mm:ss'.

## Step 2 - Call the function from Tkinter

To run your code alongside Tkinter's event loop, you need to use the `after` method provided by the Tkinter `root` object. This method schedules a function to be called after a certain amount of time, specified in milliseconds. 

To use `after`, you need to call it once from the main program and pass it your function and the delay time. For example:

```python
import tkinter as tk

root = tk.Tk()

# Create a label
label = tk.Label(root, text='')
label.pack()

# Schedule the update_label function to be called every 1000ms (1 second)
root.after(1000, update_label, label)

root.mainloop()
```

This code creates a Tkinter window with a label widget, and schedules the `update_label` function to be called every second (`1000ms`). Note that we pass the updated label widget as an argument to the function.

## Step 3 - Ensure your code is non-blocking

To ensure that your code does not block the main event loop and cause the application to become unresponsive, you should avoid any long-running or blocking operations in your function. 

For example, if your function performs a network request or a file operation that takes a long time, it's better to use a separate thread or process to handle it asynchronously. You can use the `threading` or `multiprocessing` modules provided by Python for this purpose.

## Step 4 - Handle any exceptions

If your function encounters an exception while running, you should handle it gracefully to avoid crashing the entire application. You can use the `try/except` construct to catch any exceptions and log them to a file or display them to the user.

For example, you can modify the `update_label` function to catch any exceptions and log them to the console:

```python
import datetime
import traceback

def update_label(label):
    try:
        current_time = datetime.datetime.now().strftime('%H:%M:%S')
        label.config(text=current_time)
    except Exception as e:
        traceback.print_exc()
```

This function uses the `traceback` module to print the entire stack trace of any exception that occurs to the console. You can modify it to handle exceptions in a different way depending on your needs.
