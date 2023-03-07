---
title: Generate documentation for all nested modules using sphinx autodoc
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Add the `autosummary` extension to your Sphinx configuration file and use the `automodule` directive in your index.rst file to recursively document all modules.
---

**Contents**

[TOC]

# Introduction

Sphinx is a documentation generation tool that is particularly well-suited for large projects. Sphinx's autodoc extension is one of its most powerful features, allowing for the automatic generation of documentation for Python modules based on docstrings and other metadata. In this post, we'll explore how to use Sphinx's autodoc extension to automatically generate documentation for all modules in a Python project, recursively.

# Setting up your Sphinx project

To use Sphinx's autodoc extension, you'll need to set up a Sphinx project. There are many ways to do this, but one common approach is to use the Sphinx-quickstart tool. This prompts you for some basic information about your project, then sets up a Sphinx project with some default settings.

Once you have a Sphinx project set up, you'll need to configure it to use the autodoc extension. This involves adding some settings to your `conf.py` file, which is located in the root of your Sphinx project. 

# Configuring autodoc

To configure autodoc, you'll need to add some settings to your `conf.py` file. Here's an example of what you might include:

```
# Add these imports to the top of your conf.py file
import os
import sys
import sphinx_rtd_theme

# This should point to the root of your project (or wherever your modules are located)
sys.path.insert(0, os.path.abspath('../../'))

# Enable autodoc
extensions = ['sphinx.ext.autodoc']

# Set up a default autodoc configuration
autodoc_default_options = {
    'members': True,
    'undoc-members': True,
    'show-inheritance': True,
}
```

This configuration enables autodoc and sets some default options. In this case, we're telling autodoc to include all members (functions, classes, etc.), even if they don't have docstrings; and to show inheritance relationships between classes. 

# Using autodoc to generate documentation

Once you've configured autodoc, you can use it to generate documentation automatically. To do this, you'll need to create some `.rst` files in your `docs/` directory (or whatever directory you're using to store your Sphinx documentation). 

Here's an example of what an `.rst` file might look like:

```
.. toctree::
   :maxdepth: 2
   
   module_1
   module_2
   module_3
   # ...

Module 1
========

.. automodule:: my_project.module1
   :members:
   :undoc-members:
   :show-inheritance:

Module 2
========

.. automodule:: my_project.module2
   :members:
   :undoc-members:
   :show-inheritance:

Module 3
========

.. automodule:: my_project.module3
   :members:
   :undoc-members:
   :show-inheritance:

# ...
```

This file includes a table of contents (`.. toctree::`) that lists each module in your project. For each module, it includes an `.. automodule::` directive that tells Sphinx to automatically generate documentation for that module. The `:members:`, `:undoc-members:`, and `:show-inheritance:` options are the same as the ones we set in `autodoc_default_options` in `conf.py`.

Once you've created these `.rst` files, you can generate HTML documentation by running `sphinx-build` in your `docs/` directory:

```
sphinx-build -b html . _build/html
```

This will generate HTML documentation for all of your modules, with nice-looking Sphinx formatting and a table of contents to make navigation easier. 

# Conclusion

Using Sphinx's autodoc extension to automatically generate documentation for all modules in a Python project can save a lot of time and effort compared to writing documentation by hand. By configuring autodoc and creating some `.rst` files, you can generate comprehensive documentation with just a few simple commands.
