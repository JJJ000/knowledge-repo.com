---
title: Can you explain the distinctions between feather and parquet?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Feather is a fast, lightweight binary format for storing data frames while Parquet is a columnar storage format optimized for large-scale query processing.
---

**Contents**

[TOC]

# Feather vs Parquet: File Formats for Data Science

As data scientists, we often deal with very large datasets that need to be saved and shared with others. Two popular file formats for this purpose are Feather and Parquet. Both are columnar file formats that can store complex data structures efficiently. However, they have some differences and are suitable for different use cases. 

## Feather
Feather is a lightweight, columnar file format that is designed to work well with Python and R. It was created by Wes McKinney, the creator of Pandas, and is optimized for data frames. Here are some of the main features of Feather:

* **Fast read and write:** Feather is designed to be as fast as possible when reading and writing data frames. It uses a binary format that can be memory-mapped for efficient I/O operations.

* **Cross-language compatibility:** Feather can be read and written in both Python and R, making it a good format for collaboration between the two communities.

* **Low overhead:** Feather has very low overhead compared to other file formats, which means that it can store large data frames efficiently.

* **Limited data types:** Feather supports only a limited set of data types, which includes numeric, boolean, and string data. Therefore, it is not suitable for storing complex data structures.

## Parquet
Parquet is a columnar file format that is designed for Hadoop and other big data frameworks. It was created by Cloudera and is now an open source project that is supported by many companies. Here are some of the main features of Parquet:

* **Optimized for performance:** Parquet is optimized for performance when processing large datasets. It uses compression and encoding techniques to reduce the amount of data that needs to be read from disk.

* **Schema evolution:** Parquet supports schema evolution, which means that you can add, remove, or modify columns in a table without having to rewrite the entire table.

* **Support for complex data types:** Parquet supports nested data structures, such as arrays and maps, as well as more complex data types like timestamps and decimal numbers.

* **Big data integration:** Parquet is designed to work well with Hadoop and other big data frameworks, making it a good choice for large-scale data processing.

## Conclusion
Feather and Parquet are both efficient columnar file formats that are suitable for storing and sharing large datasets. Feather is lightweight, fast, and optimized for Python and R, while Parquet is optimized for performance and supports complex data structures. The choice between the two depends on the specific use case and the tools and frameworks that you are using.
