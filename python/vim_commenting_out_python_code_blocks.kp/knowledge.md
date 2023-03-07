---
title: What is the procedure for commenting out a block of Python code in vim?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To comment out a block of Python code in Vim, visually select the block and then type `norm i#` to insert a `#` at the beginning of each line in the block.
---

**Contents**

[TOC]

1. Introduction
In Vim, commenting out a block of code means adding a comment character in front of each line of the code, so that the code is not executed when the program is run. Instead of manually typing a comment character in front of each line, Vim provides a way to easily comment out a block of code with a keyboard shortcut.

2. Select the lines to be commented out
First, use Vim's visual mode to select the lines of code that you want to comment out. Move the cursor to the beginning of the block of code, press the "v" key to enter visual mode, and then move the cursor to the end of the block of code. This will highlight the selected lines.

3. Apply the comment character
After selecting the block of code, press the colon (:) key to enter command mode, and then type "s/^/#/". This command will add a comment character (#) at the beginning of each selected line. Press the Enter key to apply the command, and the block of code will be commented out.

4. Conclusion
In summary, commenting out a block of Python code in Vim can be accomplished by using visual mode to select the lines, and then applying a comment character to each line with a command in command mode. This approach is efficient and saves time compared to manually typing a comment character in front of each line.
