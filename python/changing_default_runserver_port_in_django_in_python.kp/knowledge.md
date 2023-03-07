---
title: Reword how to alter the default runserver port in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can change the default port for Django`s runserver command by specifying the new port number with the --port flag.
---

**Contents**

[TOC]

## Introduction

When developing a Django application locally with `runserver`, it runs on port 8000 by default. However, sometimes you may want to use a different port for various reasons. This tutorial will cover how to change the default runserver port in Django using Python code.

## Method 1 - Command Line Argument

One way to change the default port is to pass it as a command-line argument when running the `runserver` command. To do this, simply add the desired port number after the `runserver` command, like so:

```
python manage.py runserver <desired_port_number>
```

For example, to run the server on port 8080, the command would be:

```
python manage.py runserver 8080
```

## Method 2 - settings.py

Another way to change the default port is to set it in your `settings.py` file. Simply add the following lines to your settings file:

```python
# sets the default runserver port to 8080
PORT = 8080
# sets the runserver command to use the PORT variable
RUNSERVER_COMMAND = ['python', 'manage.py', 'runserver', f'0.0.0.0:{PORT}']
```

This method overrides the `runserver` command with a custom list of arguments. It sets the default port to be used to 8080, and the `runserver` command to use that port.

## Method 3 - Custom Command

A more advanced method is to create a custom Django command that sets the port for `runserver`. To do this, first, create a new directory called `management` in one of your Django application directories. Inside the `management` directory, create a file called `commands.py`. Inside this file, write the following code:

```python
from django.core.management.commands.runserver import Command as RunserverCommand

class Command(RunserverCommand):
    default_port = '8080'

    def handle(self, *args, **options):
        options['addrport'] = f"0.0.0.0:{self.default_port}"
        super().handle(*args, **options)
```

This new command extends the existing `runserver` command and overrides its default port with a new default value of 8080. It then sets the `addrport` option to use this new port by default.

To run this new custom command, use the following command in the terminal:

```
python manage.py <app_name> <command_name>
```

For example, if your application name is `myapp` and the new command is called `startserver`, the command would be:

```
python manage.py myapp startserver
```

This would start the server using the new custom command.

## Conclusion

These are three methods for changing the default runserver port in Django using Python. The first method uses a command-line argument to specify the desired port number, the second method overrides the `runserver` command with a custom list of arguments in `settings.py`, and the third method creates a custom command that extends the existing `runserver` command. Choose the method that works best for your specific needs.
