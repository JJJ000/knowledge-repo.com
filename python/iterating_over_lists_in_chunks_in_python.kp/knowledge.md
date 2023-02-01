---
title: Iterating over a list in chunks means to process the list in sections, rather than all at once
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the zip() function to iterate over a list in chunks.
---

**Contents**

[TOC]

#1 Using the range() Function

The range() function can be used to iterate over a list in chunks. It takes three arguments: the starting index, the stopping index, and the size of the chunks. The following example shows how to iterate over a list in chunks of 3:

```
nums = [1,2,3,4,5,6,7,8,9,10]

for i in range(0, len(nums), 3):
    chunk = nums[i:i+3]
    print(chunk)

# Output: [1, 2, 3]
#         [4, 5, 6]
#         [7, 8, 9]
#         [10]
```

#2 Using the zip() Function

The zip() function can also be used to iterate over a list in chunks. It takes two arguments: the list to be iterated over and the size of the chunks. The following example shows how to iterate over a list in chunks of 3:

```
nums = [1,2,3,4,5,6,7,8,9,10]

for chunk in zip(*[iter(nums)]*3):
    print(list(chunk))

# Output: [1, 2, 3]
#         [4, 5, 6]
#         [7, 8, 9]
#         [10]
```

#3 Using the grouper() Function

The grouper() function from the itertools module can also be used to iterate over a list in chunks. It takes two arguments: the list to be iterated over and the size of the chunks. The following example shows how to iterate over a list in chunks of 3:

```
from itertools import grouper

nums = [1,2,3,4,5,6,7,8,9,10]

for chunk in grouper(nums, 3):
    print(list(chunk))

# Output: [1, 2, 3]
#         [4, 5, 6]
#         [7, 8, 9]
#         [10]
```

#4 Using the slice() Function

The slice() function can also be used to iterate over a list in chunks. It takes three arguments: the starting index, the stopping index, and the size of the chunks. The following example shows how to iterate over a list in chunks of 3:

```
nums = [1,2,3,4,5,6,7,8,9,10]

for i in range(0, len(nums), 3):
    chunk = nums[slice(i, i+3)]
    print(chunk)

# Output: [1, 2, 3]
#         [4, 5, 6]
#         [7, 8, 9]
#         [10]
```
