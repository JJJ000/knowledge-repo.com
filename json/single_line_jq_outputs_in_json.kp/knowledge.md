---
title: Produce jq results on one line
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jq can output the results of a query in a single line of JSON.
---

**Contents**

[TOC]

### Section 1: Installing jq

In order to use jq, you must first install it. jq can be installed on most systems with a package manager, such as apt-get or yum.

### Section 2: Using jq

Once jq is installed, you can use it to parse and manipulate JSON data. For example, you can use the following command to get the value of a key in a JSON object:

```
$ jq '.key' file.json
```

### Section 3: Outputting on a Single Line

To output the result of a jq command on a single line, you can use the -c (compact) option. For example, the following command will output the value of the key on a single line:

```
$ jq -c '.key' file.json
```

### Section 4: Outputting in Json

By default, jq will output the result as a string. To output the result as a valid JSON object, you can use the -M (monochrome) option. For example, the following command will output the value of the key as a valid JSON object on a single line:

```
$ jq -cM '.key' file.json
```
