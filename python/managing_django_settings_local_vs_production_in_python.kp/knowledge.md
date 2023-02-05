---
title: What is the best way to handle different settings for local and production environments in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The best way to manage local vs production settings in Django is to use environment variables.
---

**Contents**

[TOC]

## Section 1: Separating Settings

The most common way to manage local vs production settings in Django is to separate the settings into two files. This allows for settings to be easily changed between local and production environments.

The Django documentation recommends using a “base settings” file that contains all the settings that are shared between the local and production environments. This file should be placed in the same directory as the main settings.py file.

The “local settings” file should then contain the settings that are specific to the local environment. This file should be placed in the same directory as the main settings.py file but should be named something like “local_settings.py”.

## Section 2: Environment Variables

Another way to manage local vs production settings in Django is to use environment variables. This is especially useful when dealing with sensitive information such as passwords or API keys.

Environment variables can be set in the terminal before running the Django application. This allows for settings to be easily changed between local and production environments.

The Django documentation recommends using the “dotenv” package to manage environment variables. This package allows for environment variables to be stored in a file named “.env” and then accessed in the settings.py file.

## Section 3: Version Control

Using version control is another way to manage local vs production settings in Django. This allows for settings to be easily changed between local and production environments.

The Django documentation recommends using a version control system such as Git or Mercurial. This allows for settings to be stored in a repository and then pulled down to the local or production environment when necessary.

## Section 4: Deployment Scripts

Using deployment scripts is another way to manage local vs production settings in Django. This allows for settings to be easily changed between local and production environments.

The Django documentation recommends using a deployment script such as Fabric or Ansible. This allows for settings to be stored in the deployment scripts and then applied to the local or production environment when necessary.
