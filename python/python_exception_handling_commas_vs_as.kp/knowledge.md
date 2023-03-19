---
title: Reworded differences between using a comma and the keyword 'as' in the except clause of a Python try statement
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Both comma and `as` can be used to catch multiple exceptions in a single except block, but `as` also allows accessing the actual exception object.
---

**Contents**

[TOC]

Try...Except: Comma vs 'as' in Except

When working with exceptions in Python, there are two ways to handle the specific error that has occurred: using a comma between the exception and the variable name or using the 'as' keyword. In this article, we will explore the differences between these two approaches.

Using a Comma

When using a comma to handle exceptions, the variable name is included directly after the type of exception that was raised. Here is an example:

```python
try:
    file = open("file.txt")
except FileNotFoundError, e:
    print("File not found:", e)
```

In this example, we are trying to open a file that does not exist. If the file is not found, the `FileNotFoundError` exception will be raised and the error message will be printed to the console.

Using "as"

Instead of using a comma to specify the variable name, we can use the 'as' keyword. Here is the same example using 'as':

```python
try:
    file = open("file.txt")
except FileNotFoundError as e:
    print("File not found:", e)
```

Notice the only difference is that we use 'as' instead of a comma.

The Advantages of "as"

While either 'as' or a comma are functional for capturing the error message in the except block, there are some reasons to prefer the 'as' syntax. One advantage is simply that it is more recent and thus more modern. Another advantage of 'as' is that it is more syntactically logical because it follows other Python constructs like the 'with' statement. Additionally, using 'as' makes it easier to use the error message with concise code because it allows the exception output to be stored as a variable.

The Advantages of the Comma

The comma syntax is an older approach and generally less preferred because it is less clear: some people might think that the variable passed will always be an Exception object when in fact, this is not the case. Nonetheless, some Python codebases still use it, because it is available in both Python 2 and 3. Furthermore, it's generally more concise than the "as" variant.

Conclusion

Either approach is acceptable in modern Python development, but as a general rule, 'as' is preferred because it is more consistent with other Python constructs and usually leads to more concise and readable code. However, when working on legacy code, it can be necessary to use the comma-based approach if those projects are not yet updated to use 'as.'
