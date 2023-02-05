---
title: Running command line programs from inside python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Python can execute command line programs using the subprocess module.
---

**Contents**

[TOC]

## Using the subprocess Module

The `subprocess` module allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. This module can be used to call any command line program from within a Python script.

## Setting the Environment

Using the `env` parameter for `subprocess.run()`, you can set environment variables for the process you are calling. This is useful for setting up the environment for the command line program to use, such as setting PATH variables or setting up other environment variables.

## Capturing Output

The `subprocess.run()` method has an optional `stdout` parameter which can be used to capture the output of the command line program. The output can then be parsed or used in other ways within the Python script.

## Handling Errors

The `subprocess.run()` method also has an optional `stderr` parameter which can be used to capture any errors that occur when running the command line program. This allows the Python script to handle any errors that occur in a more graceful way than simply crashing.
