---
title: What is the method to showcase the present year in a django template?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To display the current year in a Django template, use the built-in template tag `{% now `Y` %}`.
---

**Contents**

[TOC]

# Step 1: Import the datetime module
To display the current year in a Django template in Python, you first need to import the datetime module. 

``` python
from datetime import datetime
```

# Step 2: Get the current year
Once you have imported the datetime module, you can use the now() function to get the current date and time, and then use the year attribute to get the current year.

``` python
year = datetime.now().year
```

# Step 3: Pass the year to your template
Finally, you can pass the current year to your Django template by including it as a context variable in your view function.

``` python
def your_view(request):
    year = datetime.now().year
    context = {'year': year }
    return render(request, 'your_template.html', context)
```

# Step 4: Display the year in your template
In your Django template, you can access the year variable passed from your view function using the double curly braces notation.

``` html
<p>&copy; {{ year }} Your Company Name</p>
``` 

This will display the current year in your template, and automatically update it each year.
