---
title: Reword 'how to format numbers on templates in django'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use format specifier to format numbers in Django templates in Python.
---

**Contents**

[TOC]

## Introduction

Django templates provide built-in filters that can be used to format numbers. These filters can convert numbers to different types such as integers, floats, and decimals. They can also format numbers with a specific number of decimal places or add commas to large numbers. In this article, we will discuss some common filters that can be used to format numbers in Django templates.

## Using Built-in Filters

Django provides several built-in filters that can be used to format numbers. These filters can be applied to a variable inside a template to format it according to our requirements. 

### intcomma

The `intcomma` filter adds commas to large integers to make them easier to read. For example, if we have the following variable in our context:

```python
num = 1234567890
```

We can apply the `intcomma` filter to it in our template like this:

```html
{{ num|intcomma }}
```

The output of this template code will be:

```
1,234,567,890
```

### floatformat

The `floatformat` filter formats a float number to a string that has a specified number of decimal places. For example, if we have the following variable in our context:

```python
num = 3.14159265359
```

We can apply the `floatformat` filter with 2 decimal places like this:

```html
{{ num|floatformat:2 }}
```

The output of this template code will be:

```
3.14
```

### intword

The `intword` filter converts large integers into a human-readable format with appropriate units (such as "k" for thousands and "M" for millions). For example, if we have the following variable in our context:

```python
num = 1234567890
```

We can apply the `intword` filter to it in our template like this:

```html
{{ num|intword }}
```

The output of this template code will be:

```
1.23 billion
```

## Custom Filters

We can also create our own custom filters to format numbers in Django templates. Custom filters are defined as Python functions and can be registered as template filters using the `register.filter` decorator. 

For example, let's say we want to create a custom filter that formats a number with a dollar sign and two decimal places. We can create a function called `dollars` that takes a number and returns a formatted string:

```python
@register.filter(name='dollars')
def dollars(value):
    return f"${value:.2f}"
```

We can then use this filter in our template like this:

```html
{{ num|dollars }}
```

The output of this template code will be:

```
$123.46
```

## Conclusion

In this article, we discussed some built-in filters that can be used to format numbers in Django templates. We also learned how to create custom filters using Python functions. By using these filters, we can easily format numbers according to our needs and display them in a user-friendly way in our Django web applications.
