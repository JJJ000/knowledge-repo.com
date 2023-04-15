---
title: What is the best way to format json output in a shell script?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can pretty-print JSON in a shell script using the `jq` command.
---

**Contents**

[TOC]

### Using JQ

JQ is a powerful command-line JSON processor. It can be used to pretty-print JSON in a shell script. To do this, use the following command:

```shell
jq . <file.json
```

This will print the contents of the JSON file in a pretty-printed format.

### Using Python

Python has a built-in json module that can be used to pretty-print JSON in a shell script. To do this, use the following command:

```shell
python -m json.tool <file.json
```

This will print the contents of the JSON file in a pretty-printed format.

### Using JavaScript

JavaScript also has a built-in JSON object that can be used to pretty-print JSON in a shell script. To do this, use the following command:

```shell
node -e "console.log(JSON.stringify(require('<file.json'), null, 2))"
```

This will print the contents of the JSON file in a pretty-printed format.

### Using Ruby

Ruby also has a built-in JSON library that can be used to pretty-print JSON in a shell script. To do this, use the following command:

```shell
ruby -r json -e "puts JSON.pretty_generate(JSON.parse(File.read('<file.json')))"
```

This will print the contents of the JSON file in a pretty-printed format.
