---
title: Can you guide me on upgrading to Python 3.6 using conda?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To upgrade to Python 3.6 with Conda, you can use the command conda install python=3.6.
---

**Contents**

[TOC]

# Checking Current Python Version

The first step in upgrading to Python 3.6 with Conda is to check the current version of Python you are running. This can be done by opening a terminal or command prompt and typing:

```
python --version
```

If the output shows a version of Python 3.6 or higher, congratulations! You are already running Python 3.6 or higher and do not need to upgrade. If the output shows a version lower than 3.6, continue to the next section.

# Creating an Environment with Python 3.6

The next step is to create a new Conda environment with Python 3.6. This can be done by opening a terminal or command prompt and typing:

```
conda create -n py36 python=3.6
```

This command will create a new environment called 'py36' with Python version 3.6. You can replace 'py36' with whatever you want to name your environment.

# Activating the Environment

Now that you have created a new environment with Python 3.6, you need to activate it. This can be done by typing:

```
conda activate py36
```

This command will activate the environment called 'py36'. You should see the name of the environment in your command prompt or terminal.

# Conclusion

You have now successfully upgraded to Python 3.6 with Conda by creating a new environment and activating it. You can now install packages and run Python scripts using Python 3.6 in this environment.
