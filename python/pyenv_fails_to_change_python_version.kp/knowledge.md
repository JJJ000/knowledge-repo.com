---
title: It is not possible to use pyenv to change Python versions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Make sure you have installed the desired Python version and set it as the global version with `pyenv global [version]`.
---

**Contents**

[TOC]

# Issue with pyenv not working properly
There may be several different reasons why you cannot switch Python with pyenv. Here are a few of the most common issues that people run into.

## Missing Python versions
If you are unable to switch between different versions of Python using pyenv, it is possible that you have not installed the desired versions of Python. You can check which versions of Python you have installed by using the following command:
```bash
pyenv versions
```
This will show you a list of all of the Python versions that you currently have installed. If the version that you want to switch to is not listed, you will need to install it before you can switch.

## Incorrect PATH setup
Another possible issue is that your PATH environment variable is not set up correctly. If this is the case, pyenv may not be able to find the correct version of Python. You can check your PATH by running the following command:
```bash
echo $PATH
```
If you do not see the path to the pyenv executable listed in the output, you will need to update your PATH variable to include it. You can do this by adding the following to your shell's configuration file (e.g. `~/.bashrc` or `~/.zshrc`):
```bash
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

## Issue with virtualenv
Finally, if you are using virtualenv and are still unable to switch between Python versions, it is possible that there is an issue with your virtualenv setup. In some cases, the virtualenv may be using a different version of Python than the one that you want to switch to. You can check the Python version being used by your virtualenv by running the following command:
```bash
python -V
```
If this is different from the version of Python that you want to switch to, you may need to create a new virtualenv with the correct version of Python. You can do this by running the following command:
```bash
pyenv virtualenv <desired-python-version> <new-virtualenv-name>
``` 

# Solutions
Here are some possible solutions to the issues discussed above.

## Install missing Python versions
If you do not have the desired version of Python installed, you can install it using pyenv. For example, if you want to install Python 3.9.2, you can run the following command:
```bash
pyenv install 3.9.2
```
Once this is done, you should be able to switch to the new Python version using pyenv.

## Update PATH variable
To update your PATH variable to include pyenv, add the following to your shell's configuration file:
```
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```
Once this is done, close and re-open your terminal, or run the following command to reload your configuration file:
```bash
source ~/.bashrc
```
or
```bash
source ~/.zshrc
```
You should now be able to switch between different versions of Python using pyenv. 

## Re-create virtualenvs with the desired Python versions
If you are still unable to switch between versions of Python in your virtualenvs, you may need to create new virtualenvs with the correct Python versions. You can do this using the following command:
```bash
pyenv virtualenv <desired-python-version> <new-virtualenv-name>
```
Once you have created a new virtualenv with the correct Python version, activate it using the following command:
```bash
pyenv activate <new-virtualenv-name>
```
You should now be in a virtualenv with the desired version of Python. 

## Check if the issue persists
If you have tried these solutions and are still unable to switch between Python versions using pyenv, there may be other issues at play. Try running `pyenv doctor` for more information. You can also ask for help on forums like Stack Overflow or try reaching out to the pyenv community.
