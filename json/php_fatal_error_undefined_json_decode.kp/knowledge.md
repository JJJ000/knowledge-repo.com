---
title: An undefined function error occurred in PHP when attempting to call the 'json_decode()' function
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: The json\_decode() function is not defined, so it cannot be called.
---

**Contents**

[TOC]

# Solution

## Missing Extension
The most common reason for this error is that the `json` extension is not enabled in the `php.ini` file. To enable the `json` extension, open the `php.ini` file and add the following line:

`extension=json.so`

## Check Configuration
If the extension is already enabled, then it is possible that the configuration of the `php.ini` file is incorrect. Check the configuration of the `php.ini` file to ensure that the `json` extension is correctly configured.

## Reinstall PHP
If the configuration of the `php.ini` file is correct, then it is possible that the `json` extension is not installed correctly. In this case, it is recommended to reinstall PHP to ensure that all the necessary extensions are properly installed.

## Contact Hosting Provider
If the above solutions do not work, then it is possible that the hosting provider is not providing the necessary support for the `json` extension. In this case, it is recommended to contact the hosting provider to ensure that the necessary extensions are enabled and configured correctly.
