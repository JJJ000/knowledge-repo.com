---
title: An error occurred in the mac os x environment stating that mysql_config was not found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You need to install the MySQL development headers and libraries in order for mysql\_config to be available.
---

**Contents**

[TOC]

## Introduction
When trying to install a Python package that requires MySQL connector on Mac OS X, you might encounter an error message like this:

```
EnvironmentError: mysql_config not found
```

This error occurs because the necessary configuration file for MySQL is missing on Mac OS X. In this article, we will discuss the possible causes of this error and how you can fix it.


## Check if MySQL is installed
Before proceeding with any fixes, it is essential to check whether MySQL is installed on your system. You can do this by running the following command in the Terminal:

```
which mysql
```

If MySQL is installed, you should see the path of the MySQL executable file. If not, you will need to install MySQL on your system before proceeding.


## Install MySQL Connector/C
To fix the `mysql_config not found` error, you need to install MySQL Connector/C manually. Here are the steps to do that:

1. Go to the MySQL Connector/C download page: https://dev.mysql.com/downloads/connector/c/
2. Choose your platform and download the appropriate version of Connector/C. For Mac OS X, download the DMG Archive.
3. Install the DMG file by double-clicking on it and following the installation wizard.
4. After the installation is complete, open the Terminal and run the following command:

   ```
   export PATH=$PATH:/usr/local/mysql/bin
   ```

   This command adds the MySQL binaries to your system's PATH variable, allowing you to run `mysql_config`.

5. Finally, run the command to check if `mysql_config` is installed:

   ```
   mysql_config --version
   ```

   If you see a version number, it means `mysql_config` is now installed on your system.


## Conclusion
The `mysql_config not found` error is a common issue encountered while installing Python packages that require MySQL connector on Mac OS X. By following the steps listed above, you can fix the error and install the necessary dependencies for your Python package.
