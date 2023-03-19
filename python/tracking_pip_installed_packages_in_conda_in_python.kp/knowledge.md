---
title: In an anaconda (conda) environment, what methods can I use to monitor the packages installed by pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Run the command `pip freeze > requirements.txt` in the Anaconda environment to save a list of pip-installed packages in a text file.
---

**Contents**

[TOC]

## Introduction

Anaconda is a popular distribution of the Python programming language for scientific research, data science, and machine learning. One of its key features is the ability to create independent environments that can have different versions of Python or packages installed. These environments are managed using the Conda package management system. 

When working with Anaconda environments, it's important to keep track of the packages that are installed. In this guide, we'll explore different methods to keep track of pip-installed packages in an Anaconda environment.

## Method 1: Using pip freeze

One simple method to keep track of pip-installed packages in an Anaconda environment is to use the pip freeze command. This command generates a list of all the packages and their versions installed in the environment. 

To use pip freeze, simply activate the desired environment using the following command:

```
conda activate env_name
```

Then, run the following command to generate the list of installed packages:

```
pip freeze
```

The output will be a list of package names and their version numbers, which can be saved to a file or piped to another command.

## Method 2: Using Conda list

Another method to keep track of packages installed in an Anaconda environment is to use the Conda list command. This command shows a list of all the packages installed in the current environment, including those installed via pip. 

To use Conda list, activate the desired environment using the following command:

```
conda activate env_name
```

Then, run the following command:

```
conda list
```

This will list all the packages installed in the environment, along with their version numbers and installation source (Conda or pip). 

## Method 3: Using environment.yml files

Anaconda environments can be exported to YAML format using the conda env export command. This generates a file that can be used to recreate the environment, complete with all the packages and their versions. 

To use this method, activate the desired environment:

```
conda activate env_name
```

Then, run the following command to generate the YAML file:

```
conda env export > environment.yml
```

This will create an environment.yml file in the current directory that includes all the packages and their versions in the environment. The file can then be used to recreate the environment on another system, or to share the environment with others.

## Conclusion

Keeping track of installed packages in an Anaconda environment is crucial for reproducibility and collaboration. Using methods like pip freeze, conda list, and environment.yml files can help you stay organized and ensure that you have a record of what packages are installed in each environment.
