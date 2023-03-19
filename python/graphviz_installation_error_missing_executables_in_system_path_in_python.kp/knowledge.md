---
title: After installing graphviz 2.38, ensure that the executable files of graphviz are added to the path of your system to avoid the occurrence of "runtimeerror"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Add the Graphviz bin folder to the system`s path environment variable.
---

**Contents**

[TOC]

Possible Answer:

# What is the Error Message?

The error message "RuntimeError: Make sure the Graphviz executables are on your system's path" usually appears when trying to use the Graphviz layout programs in Python, such as `dot`, `neato`, `twopi`, `circo`, or `fdp`, without having them installed or configured properly. Graphviz is a powerful tool for visualizing graphs and networks, and needs to be integrated with Python and other software through a set of libraries and commands.

# How to Install Graphviz in Python?

To install Graphviz in Python, you can use one of the following methods:

- Using a package manager, such as `pip`, `conda`, or `brew`, which can automatically download and install the latest version of Graphviz and its dependencies on your system. For example, you can run `pip install graphviz` in the command line or terminal to install the `graphviz` package that provides the `Graph` and `Digraph` classes for building and rendering graphs in Python. This should also download and install the `dot` command-line tool that is used by the `render` method of the `Graph` and `Digraph` objects.
- Downloading and installing Graphviz manually from the official website, which provides a set of binaries and installers for different platforms, such as Windows, macOS, and Linux. You can choose the appropriate package for your system, and follow the instructions to install it. After installing Graphviz, you may also need to add its executables to your system's `PATH` environment variable, so that Python can find them in the command line or terminal. For example, on Windows, you can add `C:\Program Files (x86)\Graphviz2.38\bin` to the `PATH` variable in the System Properties dialog.

# How to Check if Graphviz is Installed and Accessible?

To check if Graphviz is installed and accessible from Python, you can run the following code:

``` python
import graphviz

dot = graphviz.Graph()
dot.node('A')
dot.edge('B', 'C')
dot.render('test', view=True)
```

This code creates a simple graph with one node and one edge, and renders it to a file named `test.pdf` using the `dot` command-line tool. The `view=True` option opens the rendered file in a PDF viewer, if available. If you can see the graph in the viewer, then Graphviz is installed and accessible from Python. If you see the error message "Graphviz not found", "Graphviz not executable", or "Graphviz not in PATH", then you may need to install, configure, or update your Graphviz installation.

# How to Troubleshoot Graphviz Errors in Python?

If you encounter errors related to Graphviz in Python, you can try the following steps to troubleshoot them:

- Check if Graphviz is installed and accessible from Python, as described above. Make sure you have the latest version of Graphviz and its dependencies installed, and that the executables are added to your system's `PATH` environment variable, so that Python can find them in the command line or terminal.
- Check if the Graphviz library and version are compatible with your Python version and platform. Some versions of Graphviz may not work with some versions of Python or on some platforms, due to differences in architecture, modules, or dependencies. For example, you may need to install a specific version of Graphviz for Windows, and another version for macOS or Linux. You can check the compatibility matrix on the Graphviz website, or search online for similar issues and solutions.
- Check if there are any syntax or logic errors in your Python code that use Graphviz. For example, you may have misspelled a method or attribute, or forgot to include a required argument. You can use a debugger or a print statement to trace through your code and see where the error occurs.
- Check if there are any conflicts or overlapping installations of Graphviz or other software on your system. For example, you may have installed another version of Graphviz in a different location, or another software that uses a conflicting library or command. You can check your `PATH` variable, your `PYTHONPATH` variable, or your system's package manager to see if there are any conflicts or redundancies. You can also try to uninstall and reinstall Graphviz and its dependencies in a clean environment, or to use a virtual environment to isolate your Python environment from other software.
