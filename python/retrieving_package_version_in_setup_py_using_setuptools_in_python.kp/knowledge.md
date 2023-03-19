---
title: What is the method to obtain the version specified in the setup.py (setuptools) for my package?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use `setuptools``s `pkg\_resources` module to access the version number defined in the package`s `setup.py` file.
---

**Contents**

[TOC]

# Using setuptools-scm

One way to get the version defined in setup.py is to use `setuptools-scm` package. This package is used to manage version numbers for packages that are distributed using Setuptools. It uses the version control history to generate unique version numbers for every release.

To use `setuptools-scm`, follow the steps below.

1. Install the `setuptools-scm` package:

    ```
    pip install setuptools-scm
    ```

2. Configure your `setup.py` file to use `setuptools-scm`:

    ```
    setup(
        use_scm_version=True,
        ...
    )
    ```

3. Import `setuptools_scm` and use the `version` function to retrieve the version number:

    ```
    from setuptools_scm import version

    __version__ = version()
    ```

# Using importlib.metadata

Starting in Python 3.8, you can use the `importlib.metadata` module to retrieve package metadata, including the version number. This module comes built-in with Python, so you don't need to install any additional packages.

To use `importlib.metadata`, follow the steps below.

1. Import the `metadata` function from `importlib.metadata`:

    ```
    from importlib.metadata import metadata
    ```

2. Call the `metadata` function with your package name to retrieve the metadata:

    ```
    pkg_metadata = metadata('mypackage')
    ```

3. Access the package version from the metadata:

    ```
    __version__ = pkg_metadata['version']
    ```

# Using pkg_resources

Another way to retrieve the version number defined in `setup.py` is to use the `pkg_resources` module. This module is part of the `setuptools` package, so if you're using Setuptools to build and distribute your package, you already have it installed.

To use `pkg_resources`, follow the steps below.

1. Import the `pkg_resources` module:

    ```
    import pkg_resources
    ```

2. Use the `get_distribution` function to retrieve the distribution object for your package:

    ```
    dist = pkg_resources.get_distribution('mypackage')
    ```

3. Access the package version from the distribution object:

    ```
    __version__ = dist.version
    ```

# Parsing setup.cfg

Finally, you can also retrieve the version number by parsing the `setup.cfg` file, which is used by Setuptools to store configuration options.

Assuming that the version number is stored in the `[metadata]` section of `setup.cfg`, you can retrieve it in the following way.

1. Import the `configparser` module:

    ```
    import configparser
    ```

2. Read the `setup.cfg` file and parse it:

    ```
    config = configparser.ConfigParser()
    config.read('setup.cfg')
    ```

3. Access the version number from the `[metadata]` section:

    ```
    __version__ = config.get('metadata', 'version')
    ```
