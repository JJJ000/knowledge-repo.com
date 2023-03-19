---
title: When attempting to import a personal Python script, pycharm displays an error message indicating 'no module' is available
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Make sure the module file (Python script) is located in the same directory as the file where you are trying to import it, or add the directory containing the module file to your Python path.
---

**Contents**

[TOC]

## Section 1: Understanding the problem

PyCharm is a popular integrated development environment (IDE) used by developers worldwide. When you use PyCharm to write Python code, you may encounter an error that says 'No module' when trying to import your own module (Python script). This error occurs when PyCharm cannot locate the module you are trying to import.

## Section 2: Common causes of the 'No module' error

There are several common causes of the 'No module' error when trying to import your own module in PyCharm:

1. The module is not in the current working directory.
2. The module's file name is incorrect.
3. The module is not in a directory included in the PYTHONPATH environmental variable.
4. The module is not properly installed.

## Section 3: Solutions to the 'No module' error

There are several solutions to the 'No module' error in PyCharm:

1. Make sure the module is in the correct directory. You can move the module to the current working directory or add the directory that contains the module to the PYTHONPATH environmental variable.
2. Check that the module's file name is correct. PyCharm is case-sensitive, so make sure the file name matches the import statement exactly.
3. Add the directory that contains the module to the PYTHONPATH environmental variable. You can do this in PyCharm by going to File > Settings > Project > Project interpreter > Show all > Add.
4. Install the module using pip. If the module is not properly installed, PyCharm will not be able to locate it. You can install the module using pip by typing the command 'pip install module_name' in the terminal or command prompt.

## Section 4: Conclusion

The 'No module' error in PyCharm when trying to import your own module can be frustrating, but it is usually caused by a simple mistake. By understanding the common causes of the error and following the solutions provided above, you can get your code back up and running again.
