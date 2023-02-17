---
title: Parse JSON data in a shell script
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The jq command line tool can be used to read JSON data in a shell script.
---

**Contents**

[TOC]

# Section 1: Install jq

jq is a command line tool for parsing JSON data. It can be installed with the following command:

```sh
sudo apt-get install jq
```

# Section 2: Read the JSON File

Once jq is installed, you can read the JSON file using the following command:

```sh
cat <file_name>.json | jq
```

# Section 3: Extract Data

You can extract specific data from the JSON file using the following command:

```sh
cat <file_name>.json | jq '.<key_name>'
```

# Section 4: Store Data

You can store the extracted data in a variable for later use by using the following command:

```sh
variable_name=$(cat <file_name>.json | jq '.<key_name>')
```
