---
title: Rewording setting up to enable installation via pip from github
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Run `pip install git+https//github.com/username/repo.git` to install a package from a GitHub repository.
---

**Contents**

[TOC]

## Introduction 
Github is one of the popular platforms for hosting repositories for various programming languages. It allows developers to share their code, collaborate on projects and contribute to popular open-source projects. In Python, we can install packages directly from Github using the pip package manager, which is a python package installer. In this tutorial, we will show you how to configure pip installation to work with Github repositories.


## Prerequisites
- Anaconda, Python or any other python package management tools installed on your machine.
- Basic knowledge of using the command line.


## Cloning a Github repository
To install a package from Github using pip, you need to clone the repository to your local machine using the command line. You can do this by running the following command: 

```
git clone https://github.com/<username>/<repository_name>.git
```
To install the package from a particular branch of the repository, you can add `-b branchname` to the command.

```
git clone https://github.com/<username>/<repository_name>.git -b <branchname>
```

Once you have cloned the repository, navigate to the root directory of the package using the command line.


## Installing the package with pip
After cloning the repository, you can install the package locally using pip. To do this, navigate to the root directory of the package and run the following command:

```
pip install .
```

If the package has any dependencies on other packages, you can also install them using the `requirements.txt` file included in the repository. To install the dependencies, run the following command:

```
pip install -r requirements.txt
```


## Conclusion
In this tutorial, we have shown you how to install a package from a Github repository using pip. By following the steps outlined in this tutorial, you can easily install packages from Github repositories and start using them in your Python project. Remember to check for updates regularly and keep your packages up-to-date to ensure compatibility with other packages and the Python ecosystem.
