---
title: Rewording interrupting keyboards using python's multiprocessing pool
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Keyboard interrupts can be handled in a multiprocessing Pool by using the try-except block and closing the Pool and terminating its worker processes using the terminate() method.
---

**Contents**

[TOC]

Section 1: Introduction to Keyboard Interrupts in Python

A keyboard interrupt is a signal sent to the Python interpreter from the keyboard. It triggers a KeyboardInterrupt exception that interrupts the current execution of the program. This exception is commonly used to safely terminate a long-running program or to handle user input during runtime.

In the context of multiprocessing in Python, keyboard interrupts can be particularly useful in terminating a process pool when a user wants to stop a long-running computation. However, this functionality requires some additional setup to work correctly.

Section 2: Using Keyboard Interrupts with Multiprocessing Pool

To use keyboard interrupts with a multiprocessing pool, we need to create a custom signal handler that can gracefully terminate the pool when a keyboard interrupt occurs. We can achieve this by defining a function that takes a signal number and frame as arguments and setting this function as the signal handler for SIGINT (the signal sent on a keyboard interrupt).

Here's an example of how to define a custom signal handler function:

```
import signal

def handle_sigint(signal_num, frame):
    # Clean up resources here, like closing files or sockets
    # Terminate the worker processes in the pool
    pool.terminate()
    # Exit the main process
    exit(1)

# Set the custom signal handler
signal.signal(signal.SIGINT, handle_sigint)
```

In this function, we first perform any necessary clean-up steps, like closing files or sockets, and then terminate the worker processes in the pool by calling the `terminate()` method. Finally, we exit the main process with a status code of 1.

Section 3: Implementing Keyboard Interrupts in Multiprocessing Pool

Once we have defined our custom signal handler, we can implement keyboard interrupts in our multiprocessing pool by wrapping our pool code with a try/except block that catches the KeyboardInterrupt exception.

Here's an example of how to implement keyboard interrupts in a multiprocessing pool:

```
from multiprocessing import Pool
import signal

def handle_sigint(signal_num, frame):
    # Clean up resources here, like closing files or sockets
    # Terminate the worker processes in the pool
    pool.terminate()
    # Exit the main process
    exit(1)

# Set the custom signal handler
signal.signal(signal.SIGINT, handle_sigint)

# Define the function to be executed in parallel
def square(x):
    return x * x

if __name__ == '__main__':
    # Create a pool of worker processes
    with Pool(processes=4) as pool:
        try:
            # Map the function to a list of arguments in parallel
            results = pool.map(square, range(1000000))
            print(results)
        except KeyboardInterrupt:
            # gracefully handle Keyboard Interrupts
            pool.terminate()
            exit(1)
```

In this example, we define a function `square` that takes one argument `x` and returns its square. We create a pool of four worker processes and use the `map` method to apply the `square` function to a range of 1,000,000 integers in parallel.

The try/except block catches the KeyboardInterrupt exception and gracefully terminates the pool by calling the `terminate()` method and exiting the main process with a status code of 1.

Section 4: Conclusion

Keyboard interrupts are a useful tool in terminating long-running computations or handling user input during runtime. Implementing keyboard interrupts with multiprocessing pools in Python requires defining a custom signal handler function and wrapping our pool code in a try/except block that handles KeyboardInterrupt exceptions. With this setup, we can gracefully terminate our pool and exit our program in response to a keyboard interrupt.
