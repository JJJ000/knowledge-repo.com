---
title: What is an apt interface for inputting yes or no commands in a command line-like format?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The simplest way to get APT command line interface-like yes/no input in Python is to use the built-in `input()` function and create a loop to keep prompting the user until a valid input is received.
---

**Contents**

[TOC]

Section 1: Introduction

Python is a popular high-level programming language that has been used for a variety of purposes such as web development, machine learning, and scientific computing. Python provides various modules that make it possible to write command-line interfaces similar to those seen in Linux systems.

One common use case for such interfaces is to prompt the user with a yes or no question and then take some action based on the answer. This can be done with the built-in input function, but it requires some extra code to handle the case where the user enters something other than 'y' or 'n'. In this article, we'll show how to implement a yes/no prompt in Python that behaves similarly to the APT command line interface in Linux systems.

Section 2: Using the click module

The click module is a popular library for building command-line interfaces in Python. It provides a simple way to create commands, arguments, and options, and is well-suited for prompting users for input. Here's an example of how to use click for a yes/no prompt:

```python
import click

@click.command()
def main():
    answer = click.confirm('Do you want to continue?', default=True)
    if answer:
        # do something
        pass
    else:
        # do something else
        pass
        
if __name__ == '__main__':
    main()
```

This code defines a command with click, which prompts the user with a yes/no question and sets the default answer to 'yes'. If the user answers 'yes', the code executes some action, otherwise it executes something else.

Section 3: Using the PyInquirer module

PyInquirer is a Python package that provides a framework for building interactive command-line interfaces. It allows the developer to create complex prompts with multiple choices and input types.

Here's an example of how to use PyInquirer for a yes/no prompt:

```python
from PyInquirer import prompt, Style

questions = [
    {
        'type': 'confirm',
        'message': 'Do you want to continue?',
        'name': 'continue',
        'default': True,
    },
]

answers = prompt(questions, style=Style.from_dict({
    'question': '#b373ff bold',
    'separator': '#6c757d',
    'instruction': '',
    'answer': '#33bbff bold',
}))

if answers['continue']:
    # do something
    pass
else:
    # do something else
    pass
```

This code uses PyInquirer to create a yes/no prompt with the default answer set to 'yes'. The prompt is styled using the Style.from_dict method to customize the appearance of the prompt.

Section 4: Conclusion

In this article, we've shown how to implement a yes/no prompt in Python that behaves similarly to the APT command line interface in Linux systems. We've demonstrated two approaches: using the click module and the PyInquirer module. Both methods provide an easy way to prompt the user with a yes/no question and take some action based on the answer.
