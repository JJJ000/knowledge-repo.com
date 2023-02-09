---
title: What is the syntax for retrieving the keys from a JSON object using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `keys` operator to get the key names from a JSON object using jq.
---

**Contents**

[TOC]

## Section 1: Install jq 

In order to use jq, you must first install it on your computer. To do this, follow the instructions for your operating system found on the [jq website](https://stedolan.github.io/jq/download/).

## Section 2: Locate the JSON File

Once jq is installed, you need to locate the JSON file that you want to extract the key names from. You can either open the file in a text editor or use the command line to locate the file.

## Section 3: Use jq to Extract the Key Names

Once you have located the JSON file, you can use jq to extract the key names. To do this, use the following command:

```
jq 'keys[]' <filename>
```

This will return a list of all the key names in the JSON file.

## Section 4: Save the Output

Finally, if you want to save the output of the jq command, you can use the following command:

```
jq 'keys[]' <filename> > output.txt
```

This will save the output of the jq command to a file called output.txt.
