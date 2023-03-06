---
title: What is the procedure for utilizing an alternate Python version when installing npm?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the command `npm install --python=pythonX.X` to specify a different version of Python during NPM install where `X.X` represents the version number.
---

**Contents**

[TOC]

## Background

When installing a package with npm, it may depend on a specific version of Python to be installed on your machine. If you have multiple versions of Python installed, or if the required version is not your default Python version, you may need to specify a different version to use during the npm install process.


## Method 1: Use `npm_config_python` environment variable

One way to specify a different version of Python to use during npm install is to set the `npm_config_python` environment variable to the path of the desired Python executable. 

Here's an example command to install a package using Python 3.7 on a Unix-like system: 

```
npm config set python /usr/bin/python3.7
npm install <package-name>
```

Note that the path to your desired Python executable may be different depending on your operating system and installation details.


## Method 2: Use `--python` flag

Another way to specify a different version of Python during npm install is to use the `--python` flag with the path to the desired Python executable. 

Here's an example command to install a package using Python 3.7 on a Unix-like system:

```
npm install <package-name> --python=/usr/bin/python3.7
```

Again, note that the path to your desired Python executable may be different depending on your operating system and installation details.


## Conclusion

By using either the `npm_config_python` environment variable or the `--python` flag, you can specify a different version of Python to use during npm install. This can be helpful if you have multiple Python versions on your machine or if the required version is not your default Python version.
