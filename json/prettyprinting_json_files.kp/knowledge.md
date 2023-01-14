---
title: What is the best way to format a json file for readability?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-14 00:00:00
updated_at: 2023-01-14 00:00:00
tldr: Use the `json.dumps()` function to pretty-print a JSON file.
---

**Contents**

[TOC]

### Installing the PrettyPrint Library

PrettyPrint is a library that can be used to format and display JSON files in an easy-to-read manner. To install PrettyPrint, run the following command in your terminal:

```shell
pip install json-prettyprint
```

### Using PrettyPrint

Once PrettyPrint is installed, you can use it to format and display a JSON file. To do so, use the `json_prettyprint` command followed by the file path. For example, to prettyprint a file called `example.json`, use the following command:

```shell
json_prettyprint example.json
```

### Viewing the Output

Once the command is run, PrettyPrint will output the formatted JSON file to the terminal. You can view the output in the terminal, or you can redirect it to a file if you would like to save it. To redirect the output to a file, use the following command:

```shell
json_prettyprint example.json > output.json
```

### Customizing the Output

PrettyPrint also provides options to customize the output. For example, you can specify the indentation size and the sort order of the output. To view all available options, use the `--help` flag. For example, to view the available options for PrettyPrint, use the following command:

```shell
json_prettyprint --help
```
