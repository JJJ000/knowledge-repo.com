---
title: What are the reasons for "import *" being considered as a bad practice?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: `import *` can lead to conflicts and make code harder to read and maintain.`
---

**Contents**

[TOC]

Section 1: Name Clashes and Ambiguity
--------------------------------------

Using "import *" in Python can lead to name clashes and ambiguity because it imports all names from the module into the current namespace. This means that any existing names in the current namespace that have the same name as the imported names will be overridden. This can lead to unexpected behavior and bugs as it becomes unclear which name refers to which object. 


Section 2: Performance Issues
-----------------------------

Using "import *" can also lead to performance issues because it forces the interpreter to load all names from the module, even if not all of them are used in the current program. This can slow down the program's startup time and use unnecessary memory. In large projects, this can become a significant problem and make the code less maintainable.


Section 3: Readability and Maintenance
--------------------------------------

Importing all names with "import *" can make the code less readable and harder to maintain because it is not immediately clear which names are used in the code. This can make it difficult for other developers to understand the code and make changes or additions. It can also make it harder to debug the code when errors occur.


Section 4: Incompatibility with Linters and IDEs
-----------------------------------------------

Many Linters and IDEs will flag "import *" as an error or a warning because it goes against the principles of good coding practice. This can create problems for developers who rely on these tools to identify and catch errors in their code. Avoiding "import *" can ensure compatibility with these tools and make the code more consistent and maintainable.
