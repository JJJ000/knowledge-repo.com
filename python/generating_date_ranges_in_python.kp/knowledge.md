---
title: Generating a sequence of dates in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Using the date\_range() function from the pandas library, it is possible to create a range of dates in Python.
---

**Contents**

[TOC]

**Creating a Range of Dates Using the datetime Module**

1. Import the `datetime` module:

```python
import datetime
```

2. Create a `date` object for the start date:

```python
start_date = datetime.date(2020, 1, 1)
```

3. Create a `date` object for the end date:

```python
end_date = datetime.date(2020, 12, 31)
```

4. Create a `timedelta` object to represent the number of days between the two dates:

```python
date_delta = end_date - start_date
```

5. Create a `list` of `date` objects between the start and end dates:

```python
date_range = [start_date + datetime.timedelta(days=x) for x in range(date_delta.days + 1)]
```

**Creating a Range of Dates Using the dateutil Module**

1. Import the `dateutil` module:

```python
import dateutil
```

2. Create a `date` object for the start date:

```python
start_date = dateutil.parser.parse("2020-01-01")
```

3. Create a `date` object for the end date:

```python
end_date = dateutil.parser.parse("2020-12-31")
```

4. Create a `list` of `date` objects between the start and end dates:

```python
date_range = [start_date + dateutil.relativedelta.relativedelta(days=x) for x in range((end_date - start_date).days + 1)]
```
