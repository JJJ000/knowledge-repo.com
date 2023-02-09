---
title: What is the process for combining two JSON objects from two different files using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Using jq, you can merge two JSON objects from two files by piping the output of one file into the input of the other.
---

**Contents**

[TOC]

## Section 1: Install jq

The first step is to install jq. jq is a lightweight and flexible command-line JSON processor. It can be installed on Linux, macOS, and Windows.

## Section 2: Read the JSON Files

Once jq is installed, you can read the two JSON files using the `cat` command. For example, if the two files are named `file1.json` and `file2.json`, then you can read them by running the command:

```
cat file1.json file2.json
```

## Section 3: Merge the JSON Files

To merge the two JSON files, you can use the `jq` command. For example, if the two files are named `file1.json` and `file2.json`, then you can merge them by running the command:

```
jq -s '.[0] * .[1]' file1.json file2.json
```

## Section 4: Output the Merged JSON

Finally, you can output the merged JSON to a file using the `-o` option. For example, if the output file is named `merged.json`, then you can output the merged JSON by running the command:

```
jq -s '.[0] * .[1]' file1.json file2.json -o merged.json
```
