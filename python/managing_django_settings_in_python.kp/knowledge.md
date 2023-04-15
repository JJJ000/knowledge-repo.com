---
title: How can django developers handle settings for both development and production environments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use separate Python modules/files for development and production settings, and import the appropriate module based on the environment variable or command-line argument.
---

**Contents**

[TOC]

## Introduction
Django is an open-source Python web framework that follows the model-template-view (MTV) architectural pattern. When developing a Django project, it is important to have different settings for development and production environments. In this article, we will discuss how to manage development and production settings in Python.

## Environment Variables

One way to manage development and production settings in Django is to use environment variables. Environment variables are values that can be set outside of the application and can be accessed inside the application. 

We can define environment variables for settings such as `DEBUG`, `DATABASE_URL`, `SECRET_KEY`, and others. In our Django application, we can access these environment variables using the `os` module in Python as follows:

```python
import os

DEBUG = os.environ.get('DEBUG')
DATABASE_URL = os.environ.get('DATABASE_URL')
SECRET_KEY = os.environ.get('SECRET_KEY')
```

We can set environment variables on our local machine using the command line interface or in the hosting environment. For example, for setting environment variables in a Linux environment, we can use the `export` command as follows:

```shell
export DEBUG=True
export DATABASE_URL='postgres://user:password@localhost/dbname'
export SECRET_KEY='secret_key'
```

## Settings Module

Another way to manage development and production settings in Django is to use multiple settings modules. In this approach, we create separate settings modules for development, production, and any other environment we may have such as testing, staging, etc.

For example, we can create a `settings/development.py` module and a `settings/production.py` module. The `development.py` module can have different settings than the `production.py` module. To use these different settings modules, we can set the `DJANGO_SETTINGS_MODULE` environment variable to the desired module. 

For example, to use the `development.py` settings module, we can set the following environment variable:

```shell
export DJANGO_SETTINGS_MODULE=settings.development
```

To use the `production.py` settings module, we can set the following environment variable:

```shell
export DJANGO_SETTINGS_MODULE=settings.production
```

## Configuration Files

Another approach to manage development and production settings in Django is to use configuration files. In this approach, we create separate configuration files for each environment, such as `config/development.cfg` and `config/production.cfg`. 

We can use a package such as `configparser` to parse the configuration files and use the values in our Django application. For example, our `config/development.cfg` file can have the following contents:

```config
[Settings]
DEBUG=True
DATABASE_URL=postgres://user:password@localhost/dbname
SECRET_KEY=secret_key
```

We can then parse these values in our Django application as follows:

```python
import configparser

config = configparser.ConfigParser()
config.read('config/development.cfg')

DEBUG = config['Settings'].getboolean('DEBUG')
DATABASE_URL = config['Settings'].get('DATABASE_URL')
SECRET_KEY = config['Settings'].get('SECRET_KEY')
```

We can also set the configuration file location using an environment variable:

```shell
export CONFIG_FILE=config/development.cfg
```

```python
import configparser
import os

config_file = os.environ.get('CONFIG_FILE')
if not config_file:
    raise Exception('CONFIG_FILE environment variable not set.')

config = configparser.ConfigParser()
config.read(config_file)

DEBUG = config['Settings'].getboolean('DEBUG')
DATABASE_URL = config['Settings'].get('DATABASE_URL')
SECRET_KEY = config['Settings'].get('SECRET_KEY')
```

## Conclusion

In this article, we discussed various approaches to manage development and production settings in Django. Depending on our requirements, we can choose the approach that best suits our project. Using environment variables, settings modules or configuration files provides a more dynamic and flexible way of managing settings.
