---
title: What is a command-line utility for transforming plist files into JSON format?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The plutil command-line tool can be used to convert PLIST to JSON.
---

**Contents**

[TOC]

# Introduction
PLIST (Property List) is a hierarchical data format that is used to store data in Apple's OS X and iOS operating systems. It is similar to XML, but is more compact and can contain binary data. JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used for data exchange between applications.

# Command-line Tool
There is a command-line tool available for converting PLIST to JSON. The tool is called plutil and is included in the Apple Developer Tools. It can be used to convert a PLIST file to a JSON file by running the following command:

plutil -convert json <input_file.plist> -o <output_file.json>

# Advantages
The main advantage of using the plutil command-line tool is that it is easy to use and can be run from the command line. Additionally, it is a free tool and can be used on any Mac OS X or iOS system.

# Conclusion
The plutil command-line tool is a useful tool for converting PLIST to JSON. It is easy to use and can be run from the command line. Additionally, it is a free tool and can be used on any Mac OS X or iOS system.
