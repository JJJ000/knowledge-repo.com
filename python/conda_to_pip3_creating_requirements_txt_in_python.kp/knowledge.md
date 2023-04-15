---
title: Create a requirements.txt file for pip3 using conda
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the command `pip freeze > requirements.txt` after activating your conda environment to create a requirements.txt file for pip3.
---

**Contents**

[TOC]

Section 1: Introduction

When developing a Python project, it's common to use package managers such as Conda and pip to manage dependencies. Conda is a package manager that allows you to create isolated environments, while pip is a package manager that installs packages globally or locally. While both managers serve similar purposes, they have different file formats for specifying dependencies. In this tutorial, we will look at how to create a requirements.txt file for pip from a Conda environment.

Section 2: Conda Environment

To create a requirements.txt file for pip, we first need to activate the Conda environment we want to create the file for. To activate the environment, use the following command:

```
conda activate <environment_name>
```

Replace `<environment_name>` with the name of the Conda environment you want to activate.

Section 3: Exporting Conda environment to requirements.txt

The next step is to export the Conda environment to a YAML file using the following command:

```
conda env export > environment.yml
```

This will create a `environment.yml` file that contains all the packages and dependencies installed in the Conda environment.

Now we need to convert the `environment.yml` file to a requirements.txt file using the following command:

```
conda list --explicit > requirements.txt
```

This will create a `requirements.txt` file that contains the names of the packages and their versions.

Section 4: Conclusion

In this tutorial, we looked at how to create a requirements.txt file for pip from a Conda environment. We first activated the Conda environment, exported it to a YAML file, and then converted the YAML file to a requirements.txt file using a command. With this file, you can easily share your project's dependencies with others or recreate the environment on different machines.
