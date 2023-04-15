---
title: What is the process to activate a virtualenv within a systemd service unit?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add the path to the virtualenv`s Python executable in the ExecStart command of the systemd service unit.
---

**Contents**

[TOC]

## Section 1: Introduction to virtual environments

A virtual environment is a way to maintain dependencies for different Python projects without interfering with each other. It allows you to install packages for a specific project without affecting your system's global packages. You can create, activate, and deactivate virtual environments easily.

## Section 2: Creating a virtual environment

To create a virtual environment, you can use the following command:

```bash
python3 -m venv myenv
```

This command will create a virtual environment named `myenv` in the current directory.

## Section 3: Enabling a virtual environment in a systemd service unit

To enable a virtual environment in a systemd service unit, you need to specify the path to the Python executable within the virtual environment. You can do this by adding the `Environment` directive to the service unit file.

Here's an example of a service unit file that uses a virtual environment:

```ini
[Unit]
Description=My service

[Service]
ExecStart=/path/to/virtual/env/bin/python /path/to/script.py
WorkingDirectory=/path/to/working/directory
Environment="PATH=/path/to/virtual/env/bin"

[Install]
WantedBy=multi-user.target
```

In this example, the `ExecStart` directive specifies the path to the Python executable within the virtual environment, and the `Environment` directive sets the `PATH` environment variable to the path to the virtual environment's `bin` directory.

## Section 4: Activating a virtual environment within a service unit

You can also activate a virtual environment within a systemd service unit by using the `source` command to execute the virtual environment's `activate` script.

Here's an example of a service unit file that activates a virtual environment:

```ini
[Unit]
Description=My service

[Service]
ExecStart=/bin/bash -c 'source /path/to/virtual/env/bin/activate && /path/to/virtual/env/bin/python /path/to/script.py'
WorkingDirectory=/path/to/working/directory

[Install]
WantedBy=multi-user.target
```

In this example, the `ExecStart` directive executes a command that activates the virtual environment and then runs the Python script. The `source` command is used to execute the virtual environment's `activate` script.
