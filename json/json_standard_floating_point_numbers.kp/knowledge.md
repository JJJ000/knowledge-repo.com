---
title: The JSON format for representing floating point numbers
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Floating point numbers in JSON are represented as double-precision 64-bit binary format IEEE 754 values.
---

**Contents**

[TOC]

# IEEE 754 Standard
The IEEE 754 standard defines a binary representation for floating-point numbers in JSON. This standard is used in most programming languages and is the de facto standard for representing floating-point numbers in JSON.

# JSON Format
JSON defines a specific format for representing floating-point numbers. This format consists of a mantissa, an exponent, and a sign. The mantissa is a base-10 representation of the number, while the exponent is a base-2 representation of the number's power of 10. The sign indicates whether the number is positive or negative.

# Limitations
The IEEE 754 standard has some limitations when representing floating-point numbers in JSON. For example, the mantissa can only represent numbers up to a certain precision, and the exponent can only represent numbers up to a certain range. Additionally, the standard does not support certain features such as denormalized numbers and subnormal numbers.

# Alternatives
There are alternative representations for floating-point numbers in JSON. For example, the decimal representation uses a base-10 representation of the number and allows for more precision and range than the IEEE 754 standard. Additionally, the hexadecimal representation uses a base-16 representation of the number and allows for even more precision and range than the decimal representation.
