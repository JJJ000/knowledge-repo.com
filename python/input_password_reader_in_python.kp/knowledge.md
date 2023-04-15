---
title: Retrieve password input from standard input (stdin)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To read a password from stdin in Python, use the `getpass` module and call the `getpass()` function.
---

**Contents**

[TOC]

Section 1: Introduction

Python provides a standard library module called getpass that allows you to read a password from stdin in a secure manner. The getpass module uses the terminal’s echo functionality to mask the password as you type it, making it impossible for anyone shoulder surfing to see what you’re typing.

In this tutorial, we’ll discuss how to use the getpass module to read passwords from stdin in Python.

Section 2: Importing the getpass module

Before you can use the getpass module, you need to import it into your script. Here’s an example:

```python
import getpass
```

Section 3: Reading a password from stdin using getpass()

Once you’ve imported the getpass module, you can use its getpass() function to read a password from stdin. Here’s an example:

```python
import getpass

password = getpass.getpass(prompt='Enter your password: ')
print('Password:', password)
```

In this example, we’re using the getpass() function to prompt the user to enter their password. The prompt argument is optional and can be used to customize the prompt message.

Section 4: Conclusion

In conclusion, the getpass module provides a secure and convenient way to read passwords from stdin in Python. By using the getpass() function, you can ensure that passwords are not visible to anyone who may be standing nearby.
