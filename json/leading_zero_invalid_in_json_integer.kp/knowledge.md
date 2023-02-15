---
title: What happens if an integer in JSON starts with a zero?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Leading zeroes are not allowed in JSON because they can be interpreted as octal numbers.
---

**Contents**

[TOC]

## Reason

JSON does not allow numbers to begin with a leading zero because it can be confused with an octal number. Octal numbers are written in base 8 and begin with a zero. This can lead to unexpected results when parsing the JSON data.

## Example

For example, if a JSON data contains the number `010`, it can be confused with the octal number `8` (`010` in base 8 is equivalent to `8` in base 10). This can lead to unexpected results when parsing the JSON data.

## Solution

The solution is to avoid using numbers with leading zeroes in JSON. If the number must have a leading zero, it should be enclosed in quotes to make it a string.
