---
title: How can I resolve the "importerror cannot import name x" or "attributeerror ... (most likely due to a circular import)" errors?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Check your import statements and reorder them to avoid circular imports.
---

**Contents**

[TOC]

# Troubleshooting

1. Check for Circular Imports: A circular import is when two modules import each other. This can cause an error when one of the modules attempts to access the other module before it has finished loading. To fix this, you can either restructure your code so that the modules don't import each other, or you can use the `importlib.import_module` function to import the module in a deferred way.

2. Check for Spelling Errors: If you have misspelled the name of a module or attribute, you may get an ImportError or AttributeError. Double-check the spelling of the name and make sure it matches the name of the module or attribute you are trying to import or access.

# Prevention

1. Use Relative Imports: Relative imports can help prevent circular imports. When importing a module, use a relative import instead of an absolute import. This will ensure that the module is imported from the correct location, and it will also help prevent circular imports.

2. Use the `importlib` Module: The `importlib` module provides an easy way to import modules in a deferred way. This can help prevent circular imports and reduce the chances of getting an ImportError or AttributeError.
