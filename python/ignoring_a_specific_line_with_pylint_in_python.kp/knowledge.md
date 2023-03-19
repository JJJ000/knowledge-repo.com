---
title: Can a particular line be disregarded using pylint?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Yes, it is possible to ignore one single specific line with Pylint in Python by adding a `# pylint disable` comment at the end of the line.
---

**Contents**

[TOC]

Introduction 

Pylint is a powerful code analysis tool for Python that checks for errors, bugs, and code quality issues. It has several configuration options that allow developers to customize the analysis and ignore certain warnings. In this article, we will explore how to ignore a single specific line with Pylint in Python.

Using inline comments 

One way to ignore a single specific line with Pylint is to use an inline comment. To do this, you need to add the following comment at the end of the line:

```# pylint: disable=<message-id>```

where <message-id> is the unique identifier of the message that you want to ignore. For example, if you want to ignore the "missing docstring" warning for a specific function, you can use the following code:

```
def my_function():  # pylint: disable=missing-docstring
    print("Hello world!")
```

Using a configuration file 

Another way to ignore a single specific line with Pylint is to use a configuration file. To do this, you need to create a .pylintrc file in your project directory and add the following section:

```
[pylint.messages control]
disable=<message-id>
```

where <message-id> is the unique identifier of the message that you want to ignore. For example, if you want to ignore the "missing docstring" warning for a specific file, you can use the following code:

```
[pylint.messages control]
disable=C0111
```

Using a command-line argument 

Finally, you can ignore a single specific line with Pylint by using a command-line argument. To do this, you need to add the following argument when you run the Pylint command:

```--disable=<message-id>```

where <message-id> is the unique identifier of the message that you want to ignore. For example, if you want to ignore the "missing docstring" warning for a specific module, you can use the following command:

```pylint --disable=C0111 my_module.py```

Conclusion 

In this article, we explored how to ignore a single specific line with Pylint in Python. We showed how to use inline comments, configuration files, and command-line arguments to disable specific warnings for specific lines or modules. By using these techniques, developers can customize the analysis and focus on the most critical issues in their code.
