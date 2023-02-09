---
title: What is the best way to format a JSON block in a github wiki?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use triple backticks (```) before and after the JSON block to style it in Github Wiki.
---

**Contents**

[TOC]

## Section 1: Syntax Highlighting

In order to style a JSON block in Github Wiki, you can use syntax highlighting. This will allow you to color code the different elements of the JSON block, making it easier to read and understand. To do this, you need to wrap the JSON block in a "```json" tag, like this:

```json
{
    "name": "John Doe",
    "age": 32,
    "address": {
        "street": "123 Main Street",
        "city": "New York",
        "state": "NY"
    }
}
```

## Section 2: Formatting

Another way to style a JSON block in Github Wiki is to use formatting. This can help make the JSON block more readable and easier to understand. You can do this by using the "```jsonf" tag, like this:

```jsonf
{
    "name": "John Doe",
    "age": 32,
    "address": {
        "street": "123 Main Street",
        "city": "New York",
        "state": "NY"
    }
}
```

## Section 3: Line Breaks

You can also use line breaks to make the JSON block easier to read. This can be done by adding a "```js" tag before the JSON block, like this:

```js
{
    "name": "John Doe",
    "age": 32,
    "address": {
        "street": "123 Main Street",
        "city": "New York",
        "state": "NY"
    }
}
```

## Section 4: Comments

Finally, you can add comments to a JSON block in Github Wiki to provide additional context or explanation. To do this, you need to use the "```js-comments" tag, like this:

```js-comments
{
    "name": "John Doe", //Name of the user
    "age": 32, //Age of the user
    "address": {
        "street": "123 Main Street", //Street address
        "city": "New York", //City
        "state": "NY" //State
    }
}
```
