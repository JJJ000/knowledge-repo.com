---
title: How to convert \uxxxx unicode to utf-8 using command-line tools on a *nix system?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the command `iconv -f utf-16 -t utf-8 <file>.json > <file>\_utf8.json` to convert \uXXXX unicode to UTF-8 in a JSON file in *nix.
---

**Contents**

[TOC]

**Section 1: Install iconv**

The iconv command line utility is a great tool for converting text from one encoding to another. To install it on a *nix system, run the following command:

`sudo apt-get install iconv`

**Section 2: Convert Unicode to UTF-8**

Once iconv is installed, you can use it to convert \uXXXX unicode to UTF-8. The command to do this is:

`iconv -f UTF-16 -t UTF-8 input.txt > output.txt`

Where input.txt is the name of the file containing the \uXXXX unicode and output.txt is the name of the file that will contain the UTF-8 encoded text.

**Section 3: Convert JSON to UTF-8**

If you have a JSON file that contains \uXXXX unicode, you can convert it to UTF-8 with the following command:

`iconv -f UTF-16 -t UTF-8 input.json > output.json`

Where input.json is the name of the file containing the \uXXXX unicode and output.json is the name of the file that will contain the UTF-8 encoded JSON.

**Section 4: Verify the Conversion**

Once you have converted the \uXXXX unicode to UTF-8, you can verify that it was successful by running the following command:

`iconv -l | grep UTF-8`

This will list all of the encodings supported by iconv, and you should see UTF-8 listed in the output.
