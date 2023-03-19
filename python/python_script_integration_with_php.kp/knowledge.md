---
title: Executing a Python script through php
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You can use the `exec()` function in PHP to run a Python script.
---

**Contents**

[TOC]

Section 1: Introduction
One of the greatest strengths of programming is that different languages can be integrated together to create more complex, powerful applications. This is the case with Python and PHP, where Python scripts can be run from PHP.

Section 2: Using the exec() function
One way to run Python scripts from PHP is to use the exec() function in PHP. This function executes an external program and returns its output. To use exec() to run a Python script, the command to run the script is passed as an argument to the function. Here's an example:

```
<?php
$output = exec('python script.py');
echo $output;
?>
```

In this example, the script.py file is executed using the Python interpreter and its output is captured in the $output variable, which is then printed. Note that the script.py file should be in the same directory as the PHP script.

Section 3: Using the shell_exec() function
Another function that can be used to run Python scripts from PHP is the shell_exec() function. This function behaves similarly to exec(), but it returns the full output of the command, including any error messages. Here's an example:

```
<?php
$output = shell_exec('python script.py');
echo $output;
?>
```

In this example, the script.py file is also executed using the Python interpreter, but the output is captured in the $output variable using shell_exec() instead.

Section 4: Conclusion
In conclusion, running Python scripts from PHP is a useful way to combine the strengths of both languages. The exec() and shell_exec() functions in PHP provide efficient ways to execute Python scripts and capture their output. It's important to note that this approach has some security considerations that should be taken into account, such as ensuring that only trusted scripts are executed.
