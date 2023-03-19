---
title: What is the method to go back to a previous package in anaconda?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the command `conda install package=version` to install a specific version of a package in Anaconda.
---

**Contents**

[TOC]

# Introduction

Anaconda is an open-source platform used for data science, machine learning, and artificial intelligence. It has many packages and libraries that allow developers to work with different technologies including Python. However, sometimes a package update may cause compatibility issues and you may need to revert to a previous package. In this guide, we will discuss how to revert to a previous package in Anaconda.

# Finding the previous package version

The first step in reverting to a previous package in Anaconda is to find the version you want to install. You can search for the package version on the official Anaconda website, or you can use the `conda search` command in the Anaconda prompt. Here's an example of how to use the `conda search` command to find a specific package version.

```  
conda search numpy=1.18

```  

This command will display all the available versions of NumPy, and you can choose the one to install.

# Creating a new environment

Once you have found the previous package version, the next step is to create a new environment where you can install the package. This is because installing an older version of a package in the existing environment may cause version conflicts with other dependencies.

To create a new environment, you can use the `conda create` command in the Anaconda prompt. Here's an example of how to create a new environment named "myenv" with Python 3.8 and NumPy 1.18.

```  
conda create -n myenv python=3.8 numpy=1.18

```  

# Activating the new environment

After creating the new environment, you need to activate it before you can use it. To activate the environment, you can use the `conda activate` command in the Anaconda prompt. Here's an example of how to activate the "myenv" environment.

``` 
conda activate myenv
``` 


# Conclusion

Reverting to a previous package in Anaconda can be done by finding the desired package version, creating a new environment, and activating it. This will allow you to install and use the older package version without any compatibility issues.
