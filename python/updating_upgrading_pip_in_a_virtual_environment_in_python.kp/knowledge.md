---
title: What is the process for updating/upgrading pip within my virtual environment?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Run `pip install --upgrade pip` in the virtual environment.
---

**Contents**

[TOC]

##### Step 1: Activate the Virtual Environment

In order to update/upgrade pip itself from inside a virtual environment, first activate the virtual environment in which you want to update/upgrade pip. To do this, use the following command:

```
source <virtualenv_name>/bin/activate
```

##### Step 2: Check the Current Version of Pip

Once the virtual environment is activated, check the current version of pip installed by running the following command:

```
pip --version
```

##### Step 3: Update/Upgrade Pip

Once the current version of pip is identified, update/upgrade pip by running the following command:

```
pip install --upgrade pip
```

##### Step 4: Confirm the Updated/Upgraded Version of Pip

Finally, confirm the updated/upgraded version of pip by running the following command:

```
pip --version
```
