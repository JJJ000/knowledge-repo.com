---
title: Is it possible that even after using 'virtualenv --no-site-packages' command and pip, the global packages are still being detected?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `--no-site-packages` flag prevents the system site-packages from being used, but it does not prevent globally installed packages from being found by pip in the user`s home directory.
---

**Contents**

[TOC]

Introduction

Virtualenv is a tool used to create isolated Python environments. By default, it doesn't include any packages installed globally. However, sometimes, even after using `virtualenv --no-site-packages`, pip might still find global packages. This can happen due to several reasons. This article discusses these reasons and how to solve the issue.

Reasons why pip still finds global packages

Missing `virtualenvwrapper` installation

`virtualenvwrapper` is a set of extensions for `virtualenv` that make working with virtual environments easier. If `virtualenvwrapper` is not installed, the `$WORKON_HOME` environment variable won't be set. As a result, `virtualenv` won't be able to create an isolated environment and might use default packages installed globally.

Here's how to install `virtualenvwrapper` using pip:

```console
$ pip install virtualenvwrapper
```

Then, add the following lines to your shell startup file (e.g., ~/.bashrc or ~/.zshrc):

```sh
export WORKON_HOME=$HOME/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
source /usr/local/bin/virtualenvwrapper.sh
```

Incorrect `PATH` order

Sometimes, the `PATH` environment variable is set in a way that the global Python installation is checked before the isolated environment created by `virtualenv`. This can lead to `pip` using global packages instead of the ones installed in the virtual environment.

To solve this issue, we need to reorder the `PATH` environment variable so that the virtual environment comes first. Here's how to do this on Unix-based systems:

```console
$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/X11/bin

$ export PATH=/path/to/venv/bin:$PATH

$ echo $PATH
/path/to/venv/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/X11/bin
```

Using python3 symlink

Sometimes, even after using `virtualenv --no-site-packages`, `pip` might still use system packages rather than the ones from the virtual environment. One possible cause of this issue is using a `python3` symlink instead of a full path.

Instead of this:

```console
$ virtualenv --no-site-packages venv
```

Use this:

```console
$ virtualenv --no-site-packages /full/path/to/venv
```

Using `sudo` with pip

Using `sudo` with `pip` can make it use the system Python installation instead of the one in the virtual environment. This is because `sudo` resets the `PATH` environment variable.

To avoid this issue, do not use `sudo` with `pip`. Instead, activate the virtual environment and install packages using pip. Here's an example:

```console
$ source /path/to/venv/bin/activate

$ pip install package_name
```


Conclusion

In this article, we discussed why `virtualenv --no-site-packages` and `pip` might still find global packages in Python. We covered four possible reasons for this issue: missing `virtualenvwrapper` installation, incorrect `PATH` order, using python3 symlink, and using `sudo` with pip. By understanding these reasons, we can avoid this issue and work with virtual environments without any problems.
