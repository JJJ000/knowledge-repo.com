---
title: What are the steps to execute a jupyter notebook with the .ipynb extension from the terminal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To run an .ipynb Jupyter Notebook from terminal in Python, use the command `jupyter nbconvert --execute my\_notebook.ipynb`.
---

**Contents**

[TOC]

## Introduction
Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations, and narrative text. Jupyter Notebook files have the extension .ipynb and can be accessed and run in your browser. However, you can also run Jupyter Notebooks from the terminal using Python.

## Section 1: Installation
Before you can run Jupyter Notebooks from the terminal, you need to ensure that Jupyter is installed on your system. You can install Jupyter using pip, which is the package installer for Python. To install Jupyter, open your terminal and enter the following command:

```
pip install jupyter
```

## Section 2: Starting Jupyter
Once Jupyter is installed, you can start it by running the following command in your terminal:

```
jupyter notebook
```

This will launch Jupyter in your default browser and display the Jupyter dashboard where you can access your notebooks, create new notebooks or terminal sessions, and manage your files.

## Section 3: Running an .ipynb Notebook
To run an .ipynb Jupyter Notebook from the terminal, you can use the command line option "--NotebookApp.notebook_dir" to specify the directory where your notebook is located. You also need to specify the name of your notebook, including the .ipynb extension. For example, if your notebook is located in the "Documents" folder and the name of the notebook is "example_notebook.ipynb", you can run the following command:

```
jupyter notebook --NotebookApp.notebook_dir=Documents example_notebook.ipynb
```

This will launch the Jupyter Notebook server, open your default browser, and display the notebook for you to interact with.

## Section 4: Conclusion
Running Jupyter Notebooks from the terminal can be a powerful tool for managing and executing your projects. By following the above steps, you can easily start Jupyter from the terminal and run your .ipynb notebooks with ease.
