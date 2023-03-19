---
title: What is the method for obtaining the input from the tkinter text widget?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can get the input from the Tkinter Text Widget in Python by using the .get() method.
---

**Contents**

[TOC]

## Introduction

The Tkinter Text widget provides a way for users to input text into a tkinter GUI application. Once the user has entered text, you may want to access the information in the Text widget for further processing.

In this tutorial, we will discuss different approaches to fetch input from the Text widget in Tkinter.


## Method 1 - Using the get() method

The Text widget has a `get()` method that allows you to retrieve the text that has been entered into the widget. This method retrieves the text starting at the beginning of the widget up to the specified `endindex`.


### Example

```
import tkinter as tk

root = tk.Tk()

text_widget = tk.Text(root, height=10, width=30)
text_widget.pack()

def get_text():
    text = text_widget.get("1.0", "end-1c")
    print(text)

button = tk.Button(root, text="Get input", command=get_text)
button.pack()

root.mainloop()
```

In the above example, we are defining a function `get_text()` which fetches the text that has been entered in the Text widget. We have created a button which when clicked executes this function.


## Method 2 - Using the Bind method

Another way to retrieve input from the Text widget is to bind an event to it. This can be done using the `bind()` method available for the Text widget.

### Example

```
import tkinter as tk

root = tk.Tk()

text_widget = tk.Text(root, height=10, width=30)
text_widget.pack()

def get_text(event):
    text = text_widget.get("1.0", "end-1c")
    print(text)

text_widget.bind("<Return>", get_text)

root.mainloop()
```

In the above example, we are binding the `get_text()` function to the "Return" keypress event for the Text widget. As soon as the user hits the "Return" key, `get_text()` will be executed and the text entered in the Text widget will be fetched.


## Conclusion

Both of these methods can be used to fetch the input from the Tkinter Text widget. Which method you use will depend on your application needs. It is also possible to combine these methods for more advanced functionality.
