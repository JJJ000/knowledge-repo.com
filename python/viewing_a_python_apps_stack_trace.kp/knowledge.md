---
title: Displaying the sequence of calls that led to an error in a running Python program
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The stack trace can be printed using the traceback module, with the traceback.print\_stack() function.
---

**Contents**

[TOC]

# Section 1: Retrieving the Stack Trace
The stack trace of a running Python application can be retrieved using the `traceback` module. This is done by using the `traceback.print_stack()` method.

# Section 2: Example Usage
Below is an example of how to use the `traceback.print_stack()` method.

```
import traceback

def foo():
    traceback.print_stack()

foo()
```

# Section 3: Output
The output of the above code will be the stack trace of the application. It will look something like this:

```
  File "test.py", line 6, in foo
    traceback.print_stack()
  File "/usr/lib/python2.7/traceback.py", line 327, in print_stack
    print_list(extract_stack(f, limit), file, format)
  File "/usr/lib/python2.7/traceback.py", line 224, in extract_stack
    stack = getframeinfo(frame, context)
  File "/usr/lib/python2.7/traceback.py", line 160, in getframeinfo
    filename = getsourcefile(frame) or getfile(frame)
  File "/usr/lib/python2.7/inspect.py", line 437, in getsourcefile
    if getattr(getmodule(object, filename), '__loader__', None) is not None:
```

# Section 4: Considerations
It is important to note that the stack trace will only include the frames of the application that are currently running. If the application is paused or stopped, the stack trace will not include any frames that were previously running.
