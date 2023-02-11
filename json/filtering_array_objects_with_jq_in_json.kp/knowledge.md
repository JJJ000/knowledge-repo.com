---
title: What is the syntax for using jq to filter an array of objects based on the values of their properties?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the `select()` filter to filter an array of objects by element property values using jq in JSON.
---

**Contents**

[TOC]

**Section 1: Installing jq**

The first step is to install jq. jq is a command-line JSON processor. It can be installed on Linux, macOS, and Windows.

On Linux, you can install jq with your package manager. For example, on Ubuntu, you can install jq with the command:

```
sudo apt-get install jq
```

On macOS, you can install jq with Homebrew:

```
brew install jq
```

On Windows, you can install jq with Chocolatey:

```
choco install jq
```

**Section 2: Filtering an Array of Objects**

Once jq is installed, you can use it to filter an array of objects. To do this, you can use the `.` operator to access the properties of the objects in the array.

For example, if you have an array of objects with a `name` property, you can filter the array to only include objects with a `name` property that contains the string `John`:

```
jq '.[] | select(.name | contains("John"))'
```

**Section 3: Filtering by Multiple Properties**

You can also use jq to filter an array of objects by multiple properties. To do this, you can use the `and` operator to combine multiple filters.

For example, if you have an array of objects with a `name` and `age` property, you can filter the array to only include objects with a `name` property that contains the string `John` and an `age` property that is greater than 18:

```
jq '.[] | select(.name | contains("John") and .age > 18)'
```

**Section 4: Outputting the Result**

Finally, you can use the `-c` option to output the result as a compact JSON array:

```
jq -c '.[] | select(.name | contains("John") and .age > 18)'
```

This will output a compact JSON array of objects that match the filter criteria.
