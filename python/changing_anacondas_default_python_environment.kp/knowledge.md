---
title: What is the process of modifying the default Python environment in anaconda?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the command `conda activate environment\_name` in the terminal to activate a different Anaconda environment as the default one.
---

**Contents**

[TOC]

## Section 1: Understanding Anaconda environments

Anaconda is a software that allows users to manage multiple environments, each with different packages and libraries. By default, Anaconda comes with a base environment that contains a set of packages and tools. However, users can create multiple environments and switch between them as necessary. Each environment can have its own packages and settings independent of others.

## Section 2: Checking the current default environment

To check the current default Anaconda environment, open the Anaconda prompt or any terminal and enter the following command:

```
conda info --envs
```

This command will show a list of all available environments, with an asterisk (*) next to the current default environment.

## Section 3: Changing the default Anaconda environment

To change the default Anaconda environment, first, activate the environment that you wish to set as the default. Activate the environment using the following command:

```
conda activate myenv
```

Replace `myenv` with the name of the environment you wish to activate. Once the environment is activated, use the following command to set it as the default environment:

```
conda config --set env_prompt '({name})'
```

This command sets the environment prompt to the name of the active environment, making it the default.

## Section 4: Verifying the new default environment

To verify that the new default environment has been set correctly, close and reopen the terminal or Anaconda prompt. Then, use the `conda info --envs` command to confirm that the asterisk (*) is now next to the name of the new default environment. You can also start a new Python session and check which packages and libraries are available by default.
