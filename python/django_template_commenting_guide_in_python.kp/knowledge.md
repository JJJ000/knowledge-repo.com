---
title: What is the method of inserting comments in django templates?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Django templates use the {# comment #} tag to insert comments.
---

**Contents**

[TOC]

# Section 1: Introduction to Comments in Django Templates

Comments in Django templates are useful for leaving notes, reminders, and explanations for the developer or other collaborators. These comments are not rendered on the page, so they do not affect the HTML output.


# Section 2: Syntax for Comments in Django Templates

The syntax for comments in Django templates is similar to the syntax used for comments in Python. To start a comment in a Django template, use the `{#` symbol, and to end a comment, use the `#}` symbol. 

For example, if you want to leave a comment in a template file, you would write:

```
{% comment %} This is a comment {% endcomment %}
```

Or using the shorthand:

```
{# This is a comment #}
```


# Section 3: Best Practices for Using Comments in Django Templates

Comments are a useful tool in development, but it's important to use them judiciously. Some best practices for using comments in Django templates include:

- Use comments to explain complex or unusual code
- Don't include comments that simply state the obvious
- Remove comments that are no longer relevant or accurate


# Section 4: Conclusion

In conclusion, comments in Django templates allow developers to leave notes, explanations, and reminders for themselves and other collaborators without affecting the HTML output. By using comments judiciously and following best practices, developers can make their code more understandable and easier to maintain.
