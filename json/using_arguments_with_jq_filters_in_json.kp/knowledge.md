---
title: Supplying parameters to a jq filter
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Arguments can be passed to a jq filter by using the --arg or --argsfile flag.
---

**Contents**

[TOC]

#### Section 1: Overview

Jq is a command-line JSON processor that allows users to filter, transform, and format JSON data. It is commonly used for data extraction and manipulation. Jq filters can be passed arguments to allow for more complex transformations. 

#### Section 2: Syntax

The syntax for passing arguments to a jq filter is to include the argument in parentheses after the filter’s name. For example, if a filter is named “myfilter” and it takes a single argument, the syntax would be: 

```
myfilter(argument)
```

#### Section 3: Examples

Let's say we have the following JSON data: 

```
{
  "name": "John",
  "age": 25
}
```

We can use a jq filter to extract the age of the person: 

```
jq '.age'
```

This will return the age of the person (25). 

Now, let's say we want to use a jq filter to extract the age of the person if it is greater than 18. We can do this by passing an argument to the filter: 

```
jq '.age | select(. > 18)'
```

This will return the age of the person if it is greater than 18 (25).

#### Section 4: Conclusion

In conclusion, jq filters can be passed arguments to allow for more complex transformations. The syntax for passing arguments to a jq filter is to include the argument in parentheses after the filter’s name. Examples of using jq filters with arguments can be seen above.
