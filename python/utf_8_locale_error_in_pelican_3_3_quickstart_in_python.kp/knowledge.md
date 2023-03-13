---
title: The error "valueerror unknown locale utf-8" occurred while using pelican 3.3 and pelican-quickstart
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Set the LC\_ALL environment variable to en\_US.UTF-8 before running `pelican-quickstart`.
---

**Contents**

[TOC]

## Problem description
When trying to run the `pelican-quickstart` command to start a new Pelican project with Pelican 3.3, the following error is encountered:

```
ValueError: unknown locale: UTF-8
```

## Possible causes
This error occurs when there is a problem with the system's locale settings. The `locale` package in Python uses the system's locale settings to determine the appropriate encoding for text files, dates, times, and currencies, among other things. If the system's locale settings are not set correctly, this can cause problems with Python packages that depend on the `locale` package, including Pelican.

## Solution
To solve this problem, first, check the current locale settings of your system using the following command:

```bash
locale
```

If the output does not include the `UTF-8` character set or is not set to a valid locale for your region, you need to update your system's locale settings. This can be done by following these steps:

### Step 1: Locate the system's locale settings file
The location of the system's locale settings file may vary depending on the operating system and distribution being used. For example, on Ubuntu and Debian-based systems, the locale settings are defined in the `/etc/default/locale` file, while on Fedora and Red Hat-based systems, they are defined in the `/etc/locale.conf` file.

### Step 2: Edit the locale settings file
Open the locale settings file in a text editor and add the following line at the end of the file:

```
LC_ALL=en_US.UTF-8
```

Alternatively, if you prefer to use a different locale, replace `en_US.UTF-8` with the locale of your choice.

### Step 3: Save and exit the file
Save the changes to the file and exit the text editor.

### Step 4: Apply the updated locale settings
To apply the updated locale settings, run the following command:

```bash
locale-gen
```

This command will regenerate the system's locale data based on the updated settings in the locale settings file.

### Step 5: Verify the updated locale settings
To verify that the updated locale settings are applied correctly, run the `locale` command again. The output should now include the `UTF-8` character set and be set to the locale that you specified in the locale settings file.

Once the updated locale settings have been applied, try running the `pelican-quickstart` command again. The error should no longer occur, and you should be able to start a new Pelican project without any further issues.

## Conclusion
The `unknown locale: UTF-8` error when running the `pelican-quickstart` command in Python can be caused by invalid or missing locale settings on the system. To solve this issue, you need to update the system's locale settings file to include the correct locale and character set settings, and then regenerate the system's locale data using the `locale-gen` command. Once the updated locale settings have been applied, the `pelican-quickstart` command should run without encountering any errors.
