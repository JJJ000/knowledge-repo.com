---
title: Could you explain the meaning of square brackets in pip install?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Square brackets denote optional packages or dependencies that can be installed along with the main package using pip install in Python.
---

**Contents**

[TOC]

Square brackets in pip install command

Square brackets are used in pip install command in Python to install packages with optional dependencies. The optional dependencies are enclosed within square brackets and are not required for the package to function properly but can provide additional functionality if installed.

Syntax

pip install package-name [optional-dependency]

Example

The following command installs the requests package along with the optional dependency, security, if available:

```
pip install requests[security]
```

Section title 2: Using requirements.txt file with square brackets

The square brackets can also be used in the requirements.txt file to specify the optional dependencies for a package. The syntax is the same as that used in the pip install command.

Example

The following requirements.txt file specifies the optional dependency, psycopg2, for the package, django:

```
django
psycopg2-binary
```

Section title 3: Installing multiple packages with square brackets

Square brackets can be used to install multiple packages with optional dependencies together in a single command.

Syntax

```
pip install package1[optional-dependency1] package2[optional-dependency2] ...
```

Example

The following command installs the packages, matplotlib and pandas, along with their optional dependencies, tkinter and openpyxl, respectively:

```
pip install matplotlib[tkinter] pandas[openpyxl]
```

Section title 4: Conclusion

In conclusion, square brackets in pip install command are used to specify the optional dependencies for a package. They can also be used in the requirements.txt file and to install multiple packages with optional dependencies together.
