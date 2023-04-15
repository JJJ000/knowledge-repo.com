---
title: How to use python's glob function for multiple file extensions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `*` character to match multiple file extensions in a single call to the glob function.
---

**Contents**

[TOC]

# Introduction

Glob is a module in Python that is used to retrieve files that match a specific pattern in a directory. Often, we want to retrieve files that match multiple patterns, meaning we want to retrieve files that have multiple file extensions. In this article, we will look at how to use Glob to retrieve multiple file types.

# Retrieve Files with a Single Extension

Before we start retrieving files with multiple file types, let us look at how to retrieve files with a single extension. To retrieve all text files with the `txt` extension, we can use the following code:

```python
import glob

txt_files = glob.glob("*.txt")
print(txt_files)
```

This code will retrieve all `txt` files in the current working directory.

# Retrieve Files with Multiple Extensions

Now, let us look at how to retrieve files with multiple extensions using Glob. To retrieve all text files with the `txt` and `pdf` extensions, we can use the following code:

```python
import glob

txt_and_pdf_files = glob.glob("*.{txt,pdf}")
print(txt_and_pdf_files)
```

In this code, we use a brace expansion to specify the multiple file extensions we want to retrieve. The brace expansion is `{txt,pdf}`, and it retrieves all files that have the `txt` and `pdf` extensions.

# Exclude Files with Specific Extensions

Sometimes, we want to retrieve files with multiple extensions, but we want to exclude files with a specific extension. To do this, we can use the negation operator `{!,}` with the brace expansion.

For example, to retrieve all text files with the `txt` and `pdf` extensions, excluding files with the `doc` extension, we can use the following code:

```python
import glob

txt_and_pdf_files = glob.glob("*.{txt,pdf,!doc}")
print(txt_and_pdf_files)
```

In this code, we use the negation operator `!` with the brace expansion to exclude files with the `doc` extension.

# Conclusion

Glob is a powerful module that allows us to retrieve files that match a specific pattern in a directory. We can use brace expansions to retrieve files with multiple extensions and exclude files with specific extensions. By using these techniques, we can easily retrieve files with complex patterns in our Python programs.
