---
title: Utilizing both Python versions 2.x and 3.x within the ipython notebook
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In IPython Notebook it is possible to switch between Python 2.x and Python 3.x by using kernel-specific Jupyter notebooks or kernels.
---

**Contents**

[TOC]

Introduction
------------
IPython Notebook offers an excellent platform for data exploration, and development with Python. While Python 3 offers new and improved functionalities, a lot of code still uses Python 2.x syntax. Fortunately, IPython Notebook can utilize both Python 2.x and Python 3.x, although some care may need to be taken in setting up your environment.

Python for IPython Notebook
---------------------------
Python is an interpreter, so we can have multiple versions installed on our system. This is convenient in case some libraries do not work on a given version of Python. We can download and install the latest version of Python from the official website.
It is always useful to check that Python is installed correctly by typing `python --version` in a shell or command prompt. If multiple versions are installed, it may be necessary to explicitly specify which version of Python to use. For example, typing `python2` or `python3` would explicitly use the respective versions of Python.

Using both Python 2.x and Python 3.x in IPython Notebook
--------------------------------------------------------
There are several methods to have both Python 2.x and Python 3.x available in an IPython Notebook. One method is to create virtual environments using `conda` or `virtualenv`. Another approach is to install IPython kernel for each version of Python, so that we can switch between kernel sessions as needed. These approaches are described below.

Using conda
-----------
Conda is an open-source package management system and environment management system that runs on Windows, macOS, and Linux. We can use `conda` to create a virtual environment with Python 2.x and one with Python 3.x. We can then install IPython Notebook in both of these environments. In order to switch between the two environments, we can activate/deactivate them as needed. 

Here are the steps to achieve this:

1. Install [anaconda](https://www.anaconda.com/products/individual) or [miniconda](https://docs.conda.io/en/latest/miniconda.html)
2. Open a terminal or command prompt.
3. Run the following commands:

```
conda create -n py27 python=2.7
conda activate py27
conda install ipykernel
python -m ipykernel install --user --name=py27
conda deactivate
```

```
conda create -n py37 python=3.7
conda activate py37
conda install ipykernel
python -m ipykernel install --user --name=py37
conda deactivate
```

4. Open Jupyter Notebook
5. Select `Kernel` > `Change kernel` > `Python [conda env:py27]` or `Python [conda env:py37]`

We can now have both Python 2.x and Python 3.x environments in our Jupyter Notebook.

Using virtualenv
----------------
Here are the steps to create virtual environments using `virtualenv`.

1. Install [virtualenv](https://virtualenv.pypa.io/en/stable/installation.html)
2. Open a terminal or command prompt.
3. Run the following commands:

```
virtualenv -p python2.7 py27env
source py27env/bin/activate
pip install ipykernel
python -m ipykernel install --user --name=py27
deactivate
```

```
virtualenv -p python3.7 py37env
source py37env/bin/activate
pip install ipykernel
python -m ipykernel install --user --name=py37
deactivate
```

4. Open Jupyter Notebook
5. Select `Kernel` > `Change kernel` > `Python [py27env]` or `Python [py37env]`

We can now have both Python 2.x and Python 3.x environments in our Jupyter Notebook.

Conclusion
----------
In summary, we have seen two methods to use both Python 2.x and Python 3.x in IPython Notebook. One method is to create virtual environments using `conda` or `virtualenv`. Another method is to install separate IPython kernels for each version of Python, which can be switched as needed. With these approaches, we can utilize a wide range of Python packages to perform data exploration and development in IPython Notebook.
