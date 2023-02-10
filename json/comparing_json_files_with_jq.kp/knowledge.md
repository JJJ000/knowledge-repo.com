---
title: Comparing JSON files with jq or other command line utilities
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jq can be used to compare two JSON files by using the `==` operator.
---

**Contents**

[TOC]

## jq

jq is a command-line tool for manipulating and analyzing JSON data. It is designed to be lightweight and fast, and can be used to compare JSON files quickly and easily. 

## Comparing JSON Files

jq can be used to compare two JSON files by using the `compare` command. This command takes two JSON files as input and returns a boolean value indicating whether they are equal or not. For example, if we have two files `file1.json` and `file2.json`, we can compare them with the following command:

```
jq compare file1.json file2.json
```

The output will be either `true` or `false`, depending on whether the two files are equal or not.

## Other Tools

In addition to jq, there are other command-line tools that can be used to compare JSON files. For example, `json-diff` is a command-line tool for comparing and diffing JSON files. It can be used to compare two files and output a diff of the differences between them.

## Conclusion

In conclusion, jq is a powerful command-line tool for manipulating and analyzing JSON data. It can be used to quickly and easily compare two JSON files. Additionally, there are other command-line tools that can be used to compare and diff JSON files.
