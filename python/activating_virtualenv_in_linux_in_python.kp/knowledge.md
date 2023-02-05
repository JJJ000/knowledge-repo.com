---
title: What is the procedure for enabling virtualenv in linux?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Activate virtualenv in Linux with the command `source <env>/bin/activate`.
---

**Contents**

[TOC]

#1 Activating Virtualenv

Activating a virtual environment in Linux is a simple process, and it can be done with the following command:

```
source /path/to/virtualenv/bin/activate
```

This command will activate the virtual environment and change the prompt to show the active environment.

#2 Deactivating Virtualenv

Deactivating the virtual environment is just as easy as activating it. To deactivate the virtual environment, use the following command:

```
deactivate
```

This command will deactivate the virtual environment and return the prompt to its original state.

#3 Installing Packages

Once the virtual environment is activated, you can install packages into it using the pip command. For example, to install the requests package:

```
pip install requests
```

This command will install the requests package into the virtual environment.

#4 Accessing Packages

Once the packages are installed, you can access them in your Python code. For example, if you have installed the requests package, you can use it in your code like this:

```
import requests

r = requests.get('https://example.com')
```

This code will use the requests package to make a GET request to the specified URL.
