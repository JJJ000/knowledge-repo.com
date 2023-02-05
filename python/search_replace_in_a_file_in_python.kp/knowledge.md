---
title: What is the process for finding and replacing words in a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the replace() method of the file object to search and replace text in a file in Python.
---

**Contents**

[TOC]

# Section 1: Importing Libraries

In order to search and replace text in a file in Python, we must first import the necessary libraries. The following code imports the necessary libraries:

```python
import os
import fileinput
```

# Section 2: Defining the Search and Replace Function

Next, we must define a function that will search and replace text in a file. The following code defines a function called `search_replace` that takes two parameters: `file` and `search_replace`:

```python
def search_replace(file, search_replace):
    for line in fileinput.input(file, inplace=True):
        print(line.replace(search_replace[0], search_replace[1]), end='')
```

# Section 3: Calling the Function

Finally, we must call the `search_replace` function. The following code calls the `search_replace` function, passing in the file path and the search and replace parameters as arguments:

```python
search_replace('/path/to/file.txt', ('old_text', 'new_text'))
```

# Section 4: Verifying Changes

Once the `search_replace` function has been called, we can verify that the changes have been made by reading the file. The following code reads the file and prints out the contents to the console:

```python
with open('/path/to/file.txt', 'r') as f:
    contents = f.read()
    print(contents)
```
