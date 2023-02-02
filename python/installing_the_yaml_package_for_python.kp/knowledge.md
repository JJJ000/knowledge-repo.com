---
title: What is the process for installing the YAML package for python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Run `pip install pyyaml` in the terminal.
---

**Contents**

[TOC]

### Step 1: Install pip

The easiest way to install the yaml package is to use pip, the Python package manager. If you don't already have pip installed, you can download it from [here](https://pip.pypa.io/en/stable/installing/).

### Step 2: Install yaml

Once you have pip installed, you can use it to install the yaml package. Open up a command line and type the following command:

```
pip install pyyaml
```

This will install the yaml package for Python.

### Step 3: Verify Installation

To verify that the yaml package was installed correctly, open up a Python shell and try to import the package:

```
import yaml
```

If the import is successful, then the yaml package has been installed correctly.

### Step 4: Use yaml

Now that you have the yaml package installed, you can start using it in your Python code. For example, to parse a yaml file, you can use the following code:

```
import yaml

with open('config.yaml') as f:
    config = yaml.load(f, Loader=yaml.FullLoader)
```

This will parse the yaml file and store the data in the `config` variable.
