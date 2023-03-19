---
title: How should Python "import x" and "from x import y" statements be sorted appropriately?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Imports should be sorted alphabetically, with each `from` import group coming before regular imports of that module, and within each group, imports should be sorted alphabetically as well.
---

**Contents**

[TOC]

### Best Practices for Importing in Python

1. Avoid Wildcard Imports
Using wildcard imports (e.g. `from module import *`) can make it difficult to determine where a particular function or attribute is coming from. This can cause confusion and make it harder to maintain and debug your code. Instead, import only the necessary functions or attributes. 

2. Use Absolute Imports
Use absolute imports (e.g. `import module`) rather than relative imports (e.g. `from . import module`) as they are clearer and more reliable.

3. Use a Consistent Ordering
Import statements can quickly become cluttered and hard to read if they are not organised properly. A common way to order import statements is to group them into three sections: 

    - Standard library imports
    - Third-party package imports
    - Local module imports

By following this convention, your code will be more organized and easier to understand for both yourself and others who may need to work with your code.

4. Use Aliases Appropriately
Renaming modules or functions with aliases using the `as` keyword can make your code more readable, particularly for long module names or functions with long names that are used multiple times in a file.

In summary, to achieve a clean and readable import statement, avoid wildcard imports, use absolute imports, use a consistent ordering of import statements, and use aliases when they improve readability.
