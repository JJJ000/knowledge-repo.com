---
title: Generating a string of random characters that include uppercase letters and numbers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the string module`s `ascii\_uppercase` and `digits` constants with the random.choices() function to generate a random string with upper case letters and digits.
---

**Contents**

[TOC]

**Section 1: Using the Random Module**

The random module can be used to generate random strings with upper case letters and digits. To do this, we can use the `string.ascii_uppercase` and `string.digits` constants to generate a string of random characters.

```python
import random

# Generate a random string of length 10
length = 10
chars = string.ascii_uppercase + string.digits
random_string = ''.join(random.choice(chars) for i in range(length))

print(random_string)
```

**Section 2: Using the Secrets Module**

The secrets module can also be used to generate random strings with upper case letters and digits. To do this, we can use the `secrets.choice` function to select random characters from a string of upper case letters and digits.

```python
import secrets

# Generate a random string of length 10
length = 10
chars = string.ascii_uppercase + string.digits
random_string = ''.join(secrets.choice(chars) for i in range(length))

print(random_string)
```

**Section 3: Using the UUID Module**

The uuid module can also be used to generate random strings with upper case letters and digits. To do this, we can use the `uuid.uuid4` function to generate a random UUID, and then convert it to a string of upper case letters and digits.

```python
import uuid

# Generate a random string of length 10
length = 10
random_string = str(uuid.uuid4()).replace('-', '')[:length]

print(random_string)
```

**Section 4: Using the RandomBytes Module**

The randombytes module can also be used to generate random strings with upper case letters and digits. To do this, we can use the `randombytes.random_bytes` function to generate a random bytes object, and then convert it to a string of upper case letters and digits.

```python
import randombytes

# Generate a random string of length 10
length = 10
random_string = randombytes.random_bytes(length).hex()

print(random_string)
```
