---
title: What is the process for transforming an arbitrary basic JSON file into a csv file using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Using jq, one can convert arbitrary simple JSON to CSV by piping the JSON into jq and using the `-r` flag with the `.` operator to output the data as comma-separated values.
---

**Contents**

[TOC]

### Section 1: Install jq

jq is a command-line JSON processor. It can be installed on most systems using a package manager. For example, on Ubuntu, you can install it using apt-get:

```
sudo apt-get install jq
```

### Section 2: Parse JSON

Once jq is installed, you can use it to parse a JSON file. For example, if you have a file called `data.json`:

```json
[
  {
    "name": "John",
    "age": 30
  },
  {
    "name": "Jane",
    "age": 25
  }
]
```

You can parse it using jq:

```
jq '. | map({name, age})' data.json
```

This will output the parsed JSON:

```json
[
  {
    "name": "John",
    "age": 30
  },
  {
    "name": "Jane",
    "age": 25
  }
]
```

### Section 3: Convert to CSV

Once the JSON is parsed, you can use jq to convert it to CSV. For example, you can use the following command to convert the parsed JSON to CSV:

```
jq -r '. | map([.name, .age] | @csv) | join("\n")' data.json
```

This will output the CSV:

```
"John",30
"Jane",25
```

### Section 4: Output to File

Finally, you can output the CSV to a file using the `-o` option. For example, you can use the following command to output the CSV to a file called `data.csv`:

```
jq -r '. | map([.name, .age] | @csv) | join("\n")' data.json -o data.csv
```

This will write the CSV to the `data.csv` file.
