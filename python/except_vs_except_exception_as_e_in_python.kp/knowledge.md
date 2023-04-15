---
title: One variation is 'except' and the other one is 'except exception as e'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: except catches all exceptions while except Exception as e catches only exceptions that inherit from the base Exception class.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides a try-except block for handling exceptions that occur during runtime. When an error occurs within the try block, Python jumps to the except block and executes the code within it.

Section 2: except:
The except block can be used in two ways. The first way is by using the except keyword followed by the exception name as shown below.

        try:
            # some code that may raise an exception
        except error1:
            # handle error1
        except error2:
            # handle error2
        except:
            # handle all other exceptions

In the above code, we have used the except keyword followed by the exception name. The code within this block will only execute if an exception of the given type is raised by the code in the try block. The final except block is a catch-all block which will handle any exception that is not handled by the preceding except blocks.

Section 3: except Exception as e:
The second way to use the except block is by using the except keyword followed by the Exception class and an as clause as shown below.

        try:
            # some code that may raise an exception
        except Exception as e:
            # handle the exception e

In the above code, we have used the except keyword followed by the Exception class and an as clause. This block will handle any exception that occurs within the try block, including built-in exceptions like TypeError, ValueError, etc. We can access the exception object using the identifier e, which will contain information about the exception.

Section 4: Conclusion
The difference between except: and except Exception as e: is that the former is used to handle a specific type of exception, while the latter can be used to handle any exception that occurs within the try block. The former is more specific and allows us to handle the exception in a more targeted way, while the latter is more general and allows us to handle any exception that may occur.
