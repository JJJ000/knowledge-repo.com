---
title: Bringing data from a JSON file into r
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The jsonlite package can be used to import data from a JSON file into R.
---

**Contents**

[TOC]

### Section 1: Load the jsonlite Package

The jsonlite package is used to read and write JSON data in R. To load the package, use the library() function:

```r
library(jsonlite)
```

### Section 2: Read the JSON File

The fromJSON() function can be used to read a JSON file into R. The path to the file must be specified as an argument.

```r
data <- fromJSON("path/to/file.json")
```

### Section 3: View the Data

The data can be viewed using the str() or head() functions.

```r
str(data)
head(data)
```

### Section 4: Manipulate the Data

Once the data is loaded, it can be manipulated using the usual R functions.

```r
# Calculate the mean of a column
mean(data$column_name)

# Create a new column
data$new_column <- data$column_1 + data$column_2
```
