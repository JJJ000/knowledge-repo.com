---
title: What are the differences between 'pip freeze' and 'pip list'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Pip freeze outputs the list of installed packages along with their version whereas pip list only lists the package names.
---

**Contents**

[TOC]

Introduction 

Python is a high-level programming language that provides several tools to manage dependencies that are crucial to software development. Pip is the standard package manager for Python that helps install libraries and tools necessary for Python programming. In this article, we discuss the differences between pip freeze and pip list command and when to use them.

What is pip list?

pip list is a Python command that lists all the installed packages and their versions on the system. It shows the name of the package and its version number. This command is useful when you need to check the packages you have installed globally or within a virtual environment. The pip list command shows the packages in alphabetical order for easy navigation and searching.

Syntax: 

To get the list of all installed packages on your system or environment, run `pip list` in your command prompt or terminal.

Usage:

```python
pip list
```

Output:
```
Package            Version   
------------------ ----------
beautifulsoup4     4.8.2     
certifi            2020.4.5.1
chardet            3.0.4     
idna               2.9       
pip                20.3.3    
setuptools         41.2.0    
soupsieve          2.0       
urllib3            1.25.9    
```

What is pip freeze?

pip freeze is a command that helps create a requirements.txt file that lists all the installed packages in your current environment. The requirement.txt file contains the name of the installed packages and their versions suitable for Python installation. When sharing your code with others, you can include this file to help them install the necessary libraries with pip install -r requirements.txt. The pip freeze command ensures that you have a consistent environment, especially when working in a team.

Syntax:

To generate a requirements.txt file, use the pip freeze command followed by the output redirection operator (>) to write the output to a file.

Usage:

```python
pip freeze > requirements.txt
```

Output:

```
beautifulsoup4==4.8.2
certifi==2020.4.5.1
chardet==3.0.4
idna==2.9
soupsieve==2.0
urllib3==1.25.9
```

Difference between pip list and pip freeze

Both pip list and pip freeze are Python commands used to ease package management, but the difference between them is the output format they produce. pip list lists installed packages and their respective versions in alphabetical order for easier navigation and searching. In contrast, pip freeze creates a file with the installed packages and their versions ready to be installed in another environment.

Conclusion

In this article, we discussed the differences between pip list and pip freeze commands in Python. While pip list lists the installed packages and their respective versions in alphabetical order in the console, pip freeze creates a file that contains the installed packages and their respective versions, making it easier to manage package dependencies across different environments. Both commands are essential for package management in Python, and it would be wise to add them to your Python arsenal.
