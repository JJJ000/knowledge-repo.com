---
title: What is the process of debugging a flask application?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `print` statement or a Python debugger like `pdb` to examine data and step through code execution.
---

**Contents**

[TOC]

## Using print statements

One of the simplest ways to debug a Flask app in Python is to use print statements. You can add print statements to different parts of your code to see if they are being executed and to print out variable values. For example, if you have a view function that is not working correctly, you could add a print statement at the beginning of the function to see if it is even being called. You could also add print statements to print out the values of variables and other data structures to see if they contain the expected values.


## Using Flask's built-in debugger

Flask comes with a built-in debugger that you can use to track down issues in your application. This debugger can be enabled by setting the `debug` parameter to `True` when you create your Flask application object:

```python
app = Flask(__name__, debug=True)
```

Once you have enabled the debugger, Flask will display detailed error messages when an exception is raised in your application. These error messages will include a traceback of the call stack that led to the exception, along with information about the line numbers of the offending code.

You can also use the `debugger` function from the `werkzeug` library to set breakpoints and step through your code in a more interactive way.


## Using a Python debugger

Another option for debugging Flask applications is to use a Python debugger such as `pdb` or `ipdb`. These debuggers allow you to step through your code line-by-line, track variable values, and examine the call stack.

To use `pdb` or `ipdb` with Flask, you can insert a call to the `set_trace` function of the debugger at the point in your code where you want to start debugging:

```python
from pdb import set_trace

@app.route('/debug')
def debug():
    set_trace()
    # rest of your code
```

When you run your application and navigate to the `/debug` URL, execution will pause at the `set_trace` statement and you will be dropped into the `pdb` or `ipdb` interactive console. From there, you can use various commands to inspect your code and track down issues.


## Summary

These are just a few of the ways you can debug Flask applications in Python. Using print statements, Flask's built-in debugger, or a Python debugger can all help you find and fix issues in your code.
