---
title: When the arrow keys are pressed in Python shell, escape characters are observed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: This occurs because the arrow keys produce escape sequences that the Python shell interprets as special characters.
---

**Contents**

[TOC]

Problem Overview:
In Python Shell, when you press the arrow keys, you might see escape characters instead of navigating through the command history. This can make it difficult to edit previous commands and can be frustrating to work with. 

Solution: 

Section 1: Understanding the Cause of the Problem
The cause of this problem is that Python Shell uses a different set of escape characters to represent arrow key presses than your terminal or command prompt. This means that when you press an arrow key in Python Shell, it sends a different sequence of characters to your terminal than what your terminal expects. As a result, you end up seeing the escape characters instead of the expected behavior.

Section 2: Fixing the Problem in Windows
If you are using Windows, you can fix this problem by launching Python Shell with the -u option. This option disables the use of binary mode for stdin, stdout, and stderr which can help avoid the issue with arrow keys. Here's how you can do it:

1. Open Command Prompt
2. Type the following command and hit enter:
   - python -u
3. This will launch Python Shell with the -u option enabled and should fix the arrow key issue.  

Section 3: Fixing the Problem in MacOS or Linux
If you are using MacOS or Linux, you can fix this problem by using the rlwrap utility. Here's how you can do it:

1. Install rlwrap using the terminal package manager for your distribution. 
2. Open the terminal and type the following command:
   - rlwrap python
3. This will launch Python Shell with an rlwrap wrapper which will fix the arrow key issue. 

Section 4: Conclusion
In conclusion, seeing escape characters when pressing the arrow keys in Python Shell can be a frustrating issue, but it can be resolved. Depending on your operating system, there are different solutions to the problem. By following the steps outlined above, you can fix the problem and improve your workflow in Python Shell.
