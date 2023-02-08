---
title: Displaying multiple fields from a JSON file in a sequential order using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `-c` option to combine multiple fields into a single line, then use `--raw-output` to display the strings serially.
---

**Contents**

[TOC]

#### Section 1: Installation

The first step is to install jq. This can be done using a package manager like apt, yum, brew, or choco. 

#### Section 2: Syntax

The syntax for parsing and displaying multiple fields in a JSON serially is as follows:

```
jq '.field1, .field2, .field3' filename.json
```

Where `field1`, `field2`, and `field3` are the fields you want to parse and display.

#### Section 3: Example

For example, if you have a JSON file called `data.json` with the following content:

```
{
  "name": "John Doe",
  "age": 30,
  "location": "New York"
}
```

You can use the following command to parse and display the `name`, `age`, and `location` fields serially:

```
jq '.name, .age, .location' data.json
```

#### Section 4: Output

The output of the command will be:

```
"John Doe"
30
"New York"
```
