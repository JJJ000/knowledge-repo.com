---
title: What is the procedure for changing the default version of Python to 3.x on a mac operating system?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Run `sudo port select --set Python python3` to set Python`s default version to 3.x on OS X.
---

**Contents**

[TOC]

## Using Homebrew

1. Install Homebrew if it is not already installed:
    ```
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```
2. Install Python 3 using Homebrew:
    ```
    brew install python3
    ```
3. Make Python 3 the default version:
    ```
    brew linkapps python3
    ```

## Using pyenv

1. Install pyenv if it is not already installed:
    ```
    brew install pyenv
    ```
2. Install Python 3 using pyenv:
    ```
    pyenv install 3.x.x
    ```
3. Make Python 3 the default version:
    ```
    pyenv global 3.x.x
    ```
