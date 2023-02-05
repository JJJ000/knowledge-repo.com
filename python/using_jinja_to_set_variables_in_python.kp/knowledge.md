---
title: Assign a value to a variable in jinja
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python, variables can be set in Jinja templates using the `set` tag.
---

**Contents**

[TOC]

**Section 1: Introduction**

Jinja is a templating language used in Python applications. It enables developers to separate business logic and presentation layer. It is used to create HTML, XML or other markup formats that are returned to the user via an HTTP response. Jinja can be used to set variables in Python. This can be done by using the set() function in Jinja.

**Section 2: Setting Variables in Jinja**

The set() function in Jinja is used to set variables in Python. This function takes two arguments: the name of the variable and the value that is to be assigned to it. The syntax of the set() function is as follows:

```
{% set <variable_name> = <value> %}
```

For example, to set the variable ‘name’ to ‘John’, the following code can be used:

```
{% set name = ‘John’ %}
```

**Section 3: Using Variables in Jinja**

Once the variables are set, they can be used in the template. The syntax for using a variable is as follows:

```
{{ <variable_name> }}
```

For example, to print the value of the ‘name’ variable, the following code can be used:

```
{{ name }}
```

**Section 4: Conclusion**

In conclusion, variables can be set and used in Jinja using the set() and {{ }} functions respectively. This enables developers to separate business logic and presentation layer and create dynamic webpages.
