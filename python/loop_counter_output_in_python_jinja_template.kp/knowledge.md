---
title: What is the way to display loop counter in Python jinja template?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To output the value of the loop counter in a Python Jinja template, use the `{{ loop.index }}` or `{{ loop.counter }}` variable.
---

**Contents**

[TOC]

## Prerequisites

* Basic understanding of the Jinja2 templating engine
* A Python virtual environment with Jinja2 installed

## Step 1: Understanding loop.variable

`loop.variable` is a special variable in Jinja2 that allows you to access various attributes of a loop. When you iterate through a sequence using a for loop, Jinja2 automatically populates the `loop` variable with various attributes.

## Step 2: Accessing loop.counter

One of the most useful attributes of the `loop` variable is `loop.counter`. This gives you the current iteration number of the loop, starting from `1`.

To output the value of `loop.counter` in your template, simply use the `{{ loop.counter }}` syntax wherever you want to display it.

## Step 3: Using loop.index instead

If you want to access the iteration number starting from `0` instead of `1`, you can use the `loop.index` attribute instead.

To output the value of `loop.index` in your template, simply use the `{{ loop.index }}` syntax wherever you want to display it.

## Step 4: Example Usage

Here's an example Jinja2 template that uses `loop.counter` to display a list of items with their corresponding index number:

```
<ul>
  {% for item in items %}
    <li>{{ loop.counter }}. {{ item }}</li>
  {% endfor %}
</ul>
``` 

This will output a numbered list of items like so:

1. First Item
2. Second Item
3. Third Item
```
