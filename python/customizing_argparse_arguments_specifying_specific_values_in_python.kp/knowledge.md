---
title: Enabling the specification of certain values for an argparse argument
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can specify the allowed values for an Argparse argument by using the `choices` parameter.
---

**Contents**

[TOC]

# Intro
Argparse is a Python module that allows the user to parse arguments from the command line. The arguments can take different forms and types, such as flags, integers, strings, or lists. In some cases, it may be necessary to restrict the values that an argument can take. For example, if an argument represents a choice between several options, it should only accept those options and reject any other values. In this article, we will see how to allow specific values for an argparse argument in Python.

## Specifying choices
One way to restrict the values of an argparse argument is to specify a list of choices that it can take. This is done using the `choices` parameter when adding the argument to the parser. For example:

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--mode', choices=['train', 'test'])

args = parser.parse_args()

print(args.mode)
```

In this case, the `--mode` argument can only take the values `'train'` or `'test'`. If the user tries to enter any other value, such as `--mode predict`, the parser will raise an error.

## Using custom types
Another way to restrict the values of an argparse argument is to use a custom type that performs the validation. This is done by defining a function that takes a string as input and returns the corresponding value if it is valid, or raises an error otherwise. Then, this function is passed as the `type` parameter when adding the argument to the parser. For example:

```python
import argparse

def valid_mode(mode):
    if mode not in ['train', 'test']:
        raise argparse.ArgumentTypeError("Invalid mode")
    return mode

parser = argparse.ArgumentParser()
parser.add_argument('--mode', type=valid_mode)

args = parser.parse_args()

print(args.mode)
```

In this case, the `valid_mode` function checks if the input value is `'train'` or `'test'`, and raises an error if not. This function is then passed as the `type` parameter when adding the `--mode` argument to the parser. If the user enters an invalid mode, the parser will raise an error with the message "Invalid mode".

## Using subparsers
A more advanced way to restrict the values of an argparse argument is to use subparsers. This technique allows the user to define several sub-commands, each with its own set of arguments and values. For example:

```python
import argparse

parser = argparse.ArgumentParser()

subparsers = parser.add_subparsers(dest='command')
train_parser = subparsers.add_parser('train')
train_parser.add_argument('--epochs', type=int)

test_parser = subparsers.add_parser('test')
test_parser.add_argument('--checkpoint')

args = parser.parse_args()

if args.command == 'train':
    print(f"Training for {args.epochs} epochs")
elif args.command == 'test':
    print(f"Testing with checkpoint {args.checkpoint}")
```

In this case, the user can run the program with either `train` or `test` as the first argument, followed by their respective arguments. The `dest` parameter of the `add_subparsers` method specifies the name of the attribute that will be added to the namespace, which will contain the chosen sub-command. Then, we can use a conditional statement to check which sub-command was chosen and access its arguments. The advantage of this technique is that it allows us to specify different sets of values for each sub-command, without the risk of ambiguity or confusion. For example, we can define a set of choices for the `--mode` argument of the `train` sub-command, and a different set of choices for the `--mode` argument of the `test` sub-command.

# Outro
These are the main techniques to allow specific values for an argparse argument in Python: specifying choices, using custom types, and using subparsers. By choosing the right technique for the specific use case, we can ensure that our program is robust, user-friendly, and error-free.
