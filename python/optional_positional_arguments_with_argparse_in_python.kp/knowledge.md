---
title: What are the optional positional arguments for argparse?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Argparse positional arguments in Python can be made optional by specifying the argument as nargs=`?`.
---

**Contents**

[TOC]

## Using Optional Arguments
Optional arguments are arguments that are specified by the user, but do not need to be included in the command line for the program to run. To define optional arguments in Python using argparse, the add_argument() method must be used. The syntax for adding optional arguments is as follows:

```
parser.add_argument('-<option_name>', action='store', dest='<dest_name>', help='<help_message>', default=<default_value>)
```

where `<option_name>` is the name of the option, `<dest_name>` is the name of the variable the option value will be stored in, `<help_message>` is the help message that will be displayed when the user types -h or --help, and `<default_value>` is the value that will be used if the option is not specified.

## Using Optional Positional Arguments
Optional positional arguments are arguments that are optional for the user to provide, but if they are provided, they must appear in the correct position in the command line. To define optional positional arguments in Python using argparse, the add_argument() method must be used. The syntax for adding optional positional arguments is as follows:

```
parser.add_argument('<pos_arg_name>', nargs='?', action='store', dest='<dest_name>', help='<help_message>', default=<default_value>)
```

where `<pos_arg_name>` is the name of the positional argument, `<dest_name>` is the name of the variable the argument value will be stored in, `<help_message>` is the help message that will be displayed when the user types -h or --help, and `<default_value>` is the value that will be used if the argument is not specified.

## Using Optional Optional Arguments
Optional optional arguments are arguments that are optional for the user to provide, but if they are provided, they can appear in any position in the command line. To define optional optional arguments in Python using argparse, the add_argument() method must be used. The syntax for adding optional optional arguments is as follows:

```
parser.add_argument('-<option_name>', nargs='?', action='store', dest='<dest_name>', help='<help_message>', default=<default_value>)
```

where `<option_name>` is the name of the option, `<dest_name>` is the name of the variable the option value will be stored in, `<help_message>` is the help message that will be displayed when the user types -h or --help, and `<default_value>` is the value that will be used if the option is not specified.
