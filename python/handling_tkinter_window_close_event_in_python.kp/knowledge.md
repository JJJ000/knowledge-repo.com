---
title: What is the proper way to deal with the closing event of a window in tkinter?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can handle the window close event in Tkinter by binding the `<WM\_DELETE\_WINDOW>` protocol to a function which performs the desired actions.
---

**Contents**

[TOC]

# Handling the Window Close Event in Tkinter

## Introduction
When we create a GUI application using Tkinter, we often need to handle the window close event. In this event, we can perform some operations like saving the data, closing the file or database connection or simply terminating the application.

## Using the WM_DELETE_WINDOW protocol
One way to handle the window close event is by using the WM_DELETE_WINDOW protocol. We can specify a function that will be called when the user clicks on the close button of the window. We can use the protocol method to specify the function to be called when the window close button is clicked. Here's an example:

```python
import tkinter as tk

def on_closing():
    if messagebox.askokcancel("Quit", "Do you want to quit?"):
        root.destroy()

root = tk.Tk()
root.protocol("WM_DELETE_WINDOW", on_closing)
root.mainloop()
```

In the above code, we are using the `protocol` method to specify a function called `on_closing` which will be called when the user clicks on the close button of the window. The `on_closing` function displays a message box asking the user if they want to quit the application. If they click `OK`, the root window is destroyed, and the application terminates.

## Overriding the close() method
Another way to handle the window close event is by overriding the `close()` method of the `Tk` class. We can define our own `close()` method and perform the necessary operations before calling the default `close()` method. Here's an example:

```python
import tkinter as tk

class MyApplication(tk.Tk):
    def __init__(self):
        super().__init__()

        # create widgets here

    def close(self):
        # perform necessary operations before closing the window
        print("Closing the application...")
        super().quit()  # call the default close method

app = MyApplication()
app.mainloop()
```

In the above code, we have defined our own `close()` method which will be called when the user clicks on the close button of the window. We have overridden the default `close()` method and performed our own operations before calling the default `close()` method using `super().quit()`.

## Binding the close event
We can also bind the close event to a function using the `bind()` method. We can bind the `<Destroy>` event of the window to a function and perform the necessary operations in the function. Here's an example:

```python
import tkinter as tk

def on_close(event):
    # perform necessary operations before closing the window
    print("Closing the application...")

root = tk.Tk()
root.bind("<Destroy>", on_close)
root.mainloop()
```

In the above code, we are binding the `<Destroy>` event of the window to a function called `on_close`. The `on_close` function performs the necessary operations before closing the window.

## Conclusion
In this tutorial, we have learned about different ways to handle the window close event in Tkinter. We can use the WM_DELETE_WINDOW protocol, override the close() method or bind the close event to a function using the bind() method.
