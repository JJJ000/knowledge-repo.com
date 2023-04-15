---
title: Employing pylint in conjunction with django
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pylint can be used with Django in Python by running pylint on the Django project directory.
---

**Contents**

[TOC]

# Introduction
Pylint is a linting tool for Python that checks code for errors, coding standards and conventions using a rating system. When it comes to coding in Django, Pylint can be used to ensure that your code meets the Python coding style guide (PEP 8), and Django's best practices. 

# Setting up Pylint
To get started, you’ll need to install Pylint:
```
pip install pylint
```

Once Pylint is installed, you can run it on your Django project to check for errors in your codebase. The following command runs Pylint and outputs a report:
```
pylint my_django_project
```

However, you may get an error "E0611:No name 'django' in module", this is because pylint by default doesn't have Django's environment variables. To fix it you may use the following command instead:

```
pylint --load-plugins pylint_django my_django_project
```

This will install a plugin "pylint-django" which will allow Pylint to access necessary Django's environment and report errors accordingly.

# Disabling pylint checks
Pylint has an extensive list of checks it performs which can be overwhelming when you are starting. You might find that certain checks are not applicable or not important for your codebase. To disable certain checks, you can create a `.pylintrc` configuration file in your project root directory and specify which errors or warnings to ignore.

For example, to disable checking for print statements (which is a common complaint of Pylint) add this to your `.pylintrc`:
```
[MESSAGES CONTROL]
disable = W0511
```

# Conclusion
By using Pylint to check your Django codebase, you can ensure your code follows best practices and is easy to maintain. With the help of `.pylintrc`, you can also customize Pylint's checks to suit your coding style.
