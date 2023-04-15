---
title: Pattern to exclude from the global selection
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The glob module in Python supports exclude patterns using the `!` character before the pattern to be excluded.
---

**Contents**

[TOC]

Section 1: Introduction to Glob and Globbing

Glob is a Python module that provides methods for working with files and directories by using patterns. It is used for finding files and directories matching a specified pattern. The term 'globbing' refers to the process of matching file paths against a set of pattern rules. The glob module supports Unix style pathname patterns and it is used to search for files and directories based on these patterns.

Section 2: Using Glob for Basic Pattern Matching

To use glob, you first need to import it using the statement:

```python
import glob
```

Once you have imported the glob module, you can use it for basic pattern matching. For example, if you want to find all the files in a directory that have the file extension ".txt", you can use the following code:

```python
import glob

txt_files = glob.glob('/path/to/directory/*.txt')
```

This code will return a list of all the .txt files in the specified directory. The asterisk (*) is used as a wild card character in the pattern to match any characters that can appear in the file name.

Section 3: Exclude Patterns using Globs

To exclude some patterns from the overall search you can use negative pattern or the set difference operator. This can be done using the glob method `glob.glob(pathname, *, recursive=False)` which takes an optional `recursive` parameter which is False by default.

Negative pattern: this pattern negates the search. It means that it will return every file that doesn't match the pattern. This pattern is written by adding a negation character `!` to the pattern. For example:

```python
import glob
import os

# Find all files that don't have '.txt' extension
all_files = glob.glob('/path/to/directory/*.*')
non_txt_files = [f for f in all_files if not f.endswith('.txt')] 

# Find all files that don't have 'abc' in the name
all_files = glob.glob('/path/to/directory/*.*')
non_abc_files = [f for f in all_files if 'abc' not in os.path.basename(f)] 
```

Set difference operator: this operator returns the difference of two sets of patterns. The difference of two sets is the set of elements that are in one set but not in the other. For example:

```python
import glob

# Find all files except those that end with '.txt' or '.md'
all_files = glob.glob('/path/to/directory/*.*')
txt_and_md_files = set(glob.glob('/path/to/directory/*.txt')) | set(glob.glob('/path/to/directory/*.md'))
non_txt_and_md_files = list(set(all_files) - txt_and_md_files)
```

Section 4: Conclusion

Glob is a powerful tool for working with files and directories in Python. It provides a convenient way to search for files and directories based on patterns. By using the negative pattern or set difference operator, you can easily exclude certain patterns from the search. This makes glob an even more flexible and versatile tool for working with files and directories.
