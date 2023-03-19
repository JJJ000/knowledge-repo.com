---
title: Reading the ast of a .py file, altering it, and finally rewriting the modified source code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The process involves using the `ast` module to parse the file, modifying the AST, and then using the `astor` module to generate the modified source code.
---

**Contents**

[TOC]

## Introduction

Python Abstract Syntax Tree (AST) is a tree structure of the abstract syntactic structure of a Python program. It can be generated using the `ast` module in Python. Parsing a Python `.py` file, reading its AST, modifying it, and writing back the modified source code in Python involves the following steps:

1. Parsing the `.py` file and generating its AST
2. Traversing the AST tree and making the necessary modifications
3. Converting the modified AST back to the source code text
4. Writing the modified source code text to a `.py` file


## Parsing the .py file and generating its AST

To parse the `.py` file and generate its AST, we can use the `ast.parse()` function provided by the `ast` module. This function takes the Python source code as input and returns the root node of the AST tree.

```python
import ast

with open('file.py', 'r') as file:
    source_code = file.read()

ast_tree = ast.parse(source_code)
```

This will parse the `file.py` file and generate its corresponding AST tree.


## Traversing the AST tree and making the necessary modifications

Once we have the AST tree, we can traverse it and make the necessary modifications. This can be done by implementing a custom AST visitor class that overrides the appropriate methods for the specific changes you want to make. For example, to replace all occurrences of the variable `x` with the variable `y`, we can define a visitor class as follows:

```python
class ReplaceXwithY(ast.NodeTransformer):
    def visit_Name(self, node):
        if node.id == 'x':
            node.id = 'y'
        return node

ast_tree = ReplaceXwithY().visit(ast_tree)
```

This will traverse through the AST tree and replace all occurrences of the variable `x` with `y`.


## Converting the modified AST back to the source code text

After making the necessary modifications to the AST tree, we need to convert it back to the source code text. This can be done using the `ast.unparse()` function provided by the `ast` module. This function takes the root node of the AST tree as input and returns the corresponding Python source code string.

```python
modified_source_code = ast.unparse(ast_tree)
```

This will convert the modified AST tree back to the Python source code string.


## Writing the modified source code text to a .py file

Finally, we can write the modified source code text to a new `.py` file using the `open()` function and the `'w'` mode. 

```python
with open('modified_file.py', 'w') as file:
    file.write(modified_source_code)
```

This will create a new file `modified_file.py` with the modified source code text.
