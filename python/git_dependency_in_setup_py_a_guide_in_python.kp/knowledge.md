---
title: Can you provide guidance on how to include a git repository as a dependency in setup.py?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Add the Git repository to the `install\_requires` list in the setup.py file, using the format `git+<repository URL>@<commit ID>#egg=<package name>`.
---

**Contents**

[TOC]

## Section 1: Introduction

To include a Git repository as a dependency in Python, we use the ```setuptools``` module to create a setup.py file. This will allow us to specify our Git repository as a dependency within our Python project. In this tutorial, we will go through the step-by-step process of writing a setup.py file to include a Git repository as a dependency in Python.


## Section 2: Setting up the Git repository

First, we need to set up the Git repository. This involves creating a Git repository and pushing it to an online repository. Once this is done, we can use the URL of the online repository as the dependency in our setup.py file. Here are the steps to set up the Git repository:

1. Create a new local Git repository by running the command ```git init``` in your command line interface.
2. Add some files to the repository by running the commands ```git add <filename>``` and ```git commit``` to commit the changes.
3. Create an online repository in a Git repository host like GitHub or Bitbucket.
4. Push the local repository to the online repository by running the command ```git push <url>``` where ```<url>``` is the URL of the online repository.


## Section 3: Writing the setup.py file

Next, we need to write the setup.py file. This file specifies the details of our Python project and its dependencies. Here is an example of a basic setup.py file:

```
from setuptools import setup, find_packages

setup(
    name='myproject',
    version='1.0',
    packages=find_packages(),
    install_requires=[
        'numpy',
        'pandas',
        'git+<url>.git'
    ],
    entry_points={
        'console_scripts': [
            'myproject=myproject.cli:main',
        ],
    },
)
```

In the ```install_requires``` list, we specify the necessary packages for our project. To include the Git repository as a dependency, we use the URL of the online repository with the prefix ```git+``` to indicate that it is a Git repository. Replace ```<url>``` with the URL of the online repository. 


## Section 4: Installing the dependencies

Finally, we need to run the setup.py file to install our project and its dependencies. Here are the steps to install the dependencies:

1. Open your command line interface and navigate to the directory containing the setup.py file.
2. Run the command ```pip install -e .``` to install the package in editable mode. This allows us to make changes to our project without having to reinstall it.
3. Pip will automatically download and install the necessary packages specified in the ```install_requires``` list, including our Git repository.

With these steps, we have successfully included a Git repository as a dependency in our Python project.
