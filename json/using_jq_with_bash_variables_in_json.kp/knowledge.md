---
title: Using a bash variable with jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Pass the bash variable to jq as a string argument, enclosed in single quotes.
---

**Contents**

[TOC]

**Section 1: Introduction**

Bash is a Unix shell and command language, and jq is a lightweight and flexible command-line JSON processor. Bash variables can be passed to jq in order to manipulate JSON data. This can be useful for parsing and transforming data in various ways.

**Section 2: Syntax**

The syntax for passing a bash variable to jq is as follows: 

`jq '.field |= $VARIABLE'`

where `$VARIABLE` is the name of the bash variable. 

**Section 3: Example**

For example, if we have a bash variable `myvar` that contains the value `"hello"` and a JSON file `myfile.json` that contains the following data:

```
{
  "field1": "value1",
  "field2": "value2"
}
```

We can use the following command to pass the bash variable to jq and update the value of `field2`:

`jq '.field2 |= $myvar' myfile.json`

This will result in the following output:

```
{
  "field1": "value1",
  "field2": "hello"
}
```

**Section 4: Conclusion**

In conclusion, bash variables can be passed to jq in order to manipulate JSON data. This can be useful for parsing and transforming data in various ways. The syntax for passing a bash variable to jq is `jq '.field |= $VARIABLE'` where `$VARIABLE` is the name of the bash variable.
