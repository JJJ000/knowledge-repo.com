---
title: What are the steps to install Python modules if root access is not available?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the command `pip install --user module\_name` to install Python modules without root access.
---

**Contents**

[TOC]

## Method 1: Using the `--user` flag

One way to install Python modules without root access is by using the `--user` flag with the `pip` command. This installs the module in the user's home directory instead of the system directory, thereby not requiring root access. 

Here's the command to install a module using `--user` flag:

```
pip install --user module-name
```

This command will install the module in the `.local` directory in the user's home directory. 

## Method 2: Using a virtual environment

Another way to install Python modules without root access is by creating and using a virtual environment. A virtual environment is a self-contained environment with its own Python interpreter and installed libraries. This means that you can install any module you want without affecting the system Python installation.

Here's how to create and activate a virtual environment:

```
python -m venv myenv
source myenv/bin/activate
```

Once the virtual environment is activated, you can use `pip` to install any module you want:

```
pip install module-name
```

## Method 3: Using a package manager

If your system has a package manager like `apt` or `yum`, you can use it to install Python modules without root access. These package managers allow you to install packages as a regular user.

For example, on Debian-based systems, you can use the following command to install a module:

```
sudo apt-get install python3-module-name
```

On RedHat-based systems, you can use the following command:

```
sudo yum install python3-module-name
```

Alternatively, some package managers also allow you to install packages locally in your home directory using the `--user` flag.

## Method 4: Manually installing modules

Finally, you can manually install Python modules without root access by downloading the source code and installing it in your home directory.

Here's how to do it:

1. Download the source code of the module you want to install.

2. Extract the source code to a directory in your home directory.

3. Navigate to the directory containing the source code.

4. Run the following command to install the module:

   ```
   python setup.py install --user
   ```

This will install the module in your home directory without requiring root access.
