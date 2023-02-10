---
title: Construct a JSON string using bash variables
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The Bash variables can be used to construct a valid JSON string by enclosing the variables in double quotes and separating them with commas.
---

**Contents**

[TOC]

##### Section 1: Setting Bash Variables

We can create Bash variables for our JSON string in the following way:

```sh
name="John Doe"
age=25
city="New York"
```

##### Section 2: Building the JSON String

We can use the Bash variables to build a JSON string in the following way:

```sh
json="{\"name\":\"$name\",\"age\":$age,\"city\":\"$city\"}"
```

##### Section 3: Outputting the JSON String

We can output the JSON string with the following command:

```sh
echo $json
```

##### Section 4: Result

The result of the above command will be the following JSON string:

```json
{"name":"John Doe","age":25,"city":"New York"}
```
