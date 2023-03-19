---
title: What is the equivalent of virtualenv in ruby?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Rbenv is the Ruby equivalent of virtualenv in Python, used for creating isolated Ruby environments.
---

**Contents**

[TOC]

## Introduction
Virtualenv is a tool in Python that creates an isolated Python environment for projects. It allows users to install packages and libraries specific to the project without interfering with the other projects' dependencies in the system. In Ruby, RVM (Ruby Version Manager) and rbenv are two popular tools that provide similar functionalities. 

## RVM (Ruby Version Manager)
RVM is a command-line tool that manages multiple versions of Ruby and their corresponding gems. It enables users to change the active Ruby version and maintain separate gemsets for different environments. The gemsets can be switched easily using RVM's `use` command. 

To install RVM on Ubuntu, run the following command in the terminal:

```
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

This command downloads and installs RVM along with the stable version of Ruby. To create a new gemset, use the `rvm gemset create` command followed by the gemset name:

```
rvm gemset create mygemset
```

Once the gemset is created, activate it using the `rvm gemset use` command:

```
rvm gemset use mygemset
```

Now, any gems installed using `gem install` will be stored in the `mygemset` for the current Ruby version. 

## rbenv
rbenv is another popular Ruby version manager that allows users to switch between multiple versions of Ruby on a per-project basis. It also provides the ability to create virtual environments called "shims" that isolate project-specific gems. 

To install rbenv on Ubuntu, run the following commands in the terminal:

```
sudo apt-get update
sudo apt-get install rbenv
```

To create a new virtual environment, use the `rbenv virtualenv` command followed by the desired Ruby version and virtual environment name:

```
rbenv virtualenv 2.7.1 myenv
```

Now, activate the virtual environment using `rbenv local` command, followed by the Ruby version and virtual environment name:

```
rbenv local 2.7.1 myenv
```

This will set the current directory to the Ruby version and virtual environment specified. 

## Conclusion
Both RVM and rbenv are popular Ruby version managers that provide similar functionalities to virtualenv in Python. RVM offers the ability to manage multiple versions of Ruby and maintain separate gemsets for different environments, while rbenv allows users to switch between multiple versions of Ruby on a per-project basis and create virtual environments to isolate project-specific gems.
