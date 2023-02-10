---
title: Reword 'jq output based on conditions'
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Json can be used to output data conditionally based on specified criteria.
---

**Contents**

[TOC]

## Conditional Output
Conditional output allows developers to use specific values in a JSON output based on certain conditions. This can be useful for creating dynamic responses that are tailored to the user or situation.

## Basic Syntax
The basic syntax for conditional output in JSON is to use the ternary operator. This operator is used to check a condition, and then output a specific value based on the result of the check. The syntax looks like this: 

```
condition ? value_if_true : value_if_false
```

## Examples
Here are some examples of how to use the ternary operator for conditional output in JSON:

```
{
    "status": (age > 18) ? "adult" : "minor"
}
```

In this example, the value of the "status" key will be "adult" if the age is greater than 18, or "minor" if the age is less than or equal to 18.

```
{
    "message": (score > 90) ? "Excellent work!" : "Keep trying!"
}
```

In this example, the value of the "message" key will be "Excellent work!" if the score is greater than 90, or "Keep trying!" if the score is less than or equal to 90.

## Nested Conditions
It is also possible to use nested conditions for more complex logic. For example, this code will output a different message based on the value of the score:

```
{
    "message": (score > 90) ? "Excellent work!" : (score > 75) ? "Good job!" : "Keep trying!"
}
```

If the score is greater than 90, the message will be "Excellent work!" If the score is greater than 75 but less than or equal to 90, the message will be "Good job!". If the score is less than or equal to 75, the message will be "Keep trying!".
