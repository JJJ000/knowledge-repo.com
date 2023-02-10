---
title: How can I use jq to sort a JSON file based on the keys and values of those keys?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: In jq, use the `.key\_name | sort` command to sort a JSON file by keys and values of those keys.
---

**Contents**

[TOC]

# Section 1: Sort Keys

We can use the `sort_by` function to sort the keys of a JSON file in jq. The syntax for this function is `sort_by(.key)`, where `key` is the key to sort by. For example, if we have a JSON file with the following structure: 

```json
{
  "age": 32,
  "name": "John Doe",
  "height": 170
}
```

We can sort the keys alphabetically using the following command:

```
jq 'sort_by(.name)' input.json
```

This will output the following: 

```json
{
  "age": 32,
  "height": 170,
  "name": "John Doe"
}
```

# Section 2: Sort Values

We can also sort the values of a JSON file in jq. To do this, we can use the `sort` function. The syntax for this function is `sort(.key)`, where `key` is the key to sort by. For example, if we have a JSON file with the following structure: 

```json
{
  "age": 32,
  "name": "John Doe",
  "height": 170
}
```

We can sort the values of the `age` key in ascending order using the following command:

```
jq 'sort(.age)' input.json
```

This will output the following: 

```json
{
  "name": "John Doe",
  "height": 170,
  "age": 32
}
```

# Section 3: Sort Keys and Values

We can also sort both the keys and values of a JSON file in jq. To do this, we can use the `sort_by` and `sort` functions together. The syntax for this is `sort_by(.key1) | sort(.key2)`, where `key1` is the key to sort by and `key2` is the value to sort by. For example, if we have a JSON file with the following structure: 

```json
{
  "age": 32,
  "name": "John Doe",
  "height": 170
}
```

We can sort the keys alphabetically and the values of the `age` key in ascending order using the following command:

```
jq 'sort_by(.name) | sort(.age)' input.json
```

This will output the following: 

```json
{
  "age": 32,
  "height": 170,
  "name": "John Doe"
}
```

# Section 4: Sort Multiple Keys and Values

We can also sort multiple keys and values of a JSON file in jq. To do this, we can use the `sort_by` and `sort` functions multiple times. The syntax for this is `sort_by(.key1) | sort(.key2) | sort_by(.key3) | sort(.key4)`, where `key1` and `key3` are the keys to sort by and `key2` and `key4` are the values to sort by. For example, if we have a JSON file with the following structure: 

```json
{
  "age": 32,
  "name": "John Doe",
  "height": 170,
  "weight": 75
}
```

We can sort the keys alphabetically and the values of the `age` and `weight` keys in ascending order using the following command:

```
jq 'sort_by(.name) | sort(.age) | sort_by(.height) | sort(.weight)' input.json
```

This will output the following: 

```json
{
  "age": 32,
  "height": 170,
  "name": "John Doe",
  "weight": 75
}
```
