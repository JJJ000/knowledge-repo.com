---
title: In 2012, what made pandas merges in Python faster than data.table merges in r?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Python pandas had a more efficient merge algorithm and CPU utilization compared to data.table in R at that time.
---

**Contents**

[TOC]

Introduction

Pandas is a popular data analysis library in Python, whereas data.table is a popular package for data manipulation in R. In 2012, a benchmark was conducted to compare the performance of Pandas merges in Python and data.table merges in R. Interestingly, the results showed that Pandas merges were faster than data.table merges in R. In this article, we'll explore why this was the case.

Data Structures

Pandas and data.table have different data structures that impact their merge performance. Pandas primarily uses data frames, which are mutable and can be modified in place. On the other hand, data.table uses data tables, which are immutable and cannot be modified in place. Due to this difference, Pandas can optimize memory allocation and minimize copying while merging, leading to faster performance.

Parallel Execution

Another factor that contributed to the faster performance of Pandas merges in 2012 was parallel execution. Pandas had just introduced parallel execution capability, which allowed the merge to be split into multiple jobs that could be executed in parallel. This allowed for quicker execution, especially on multi-core machines. Data.table, however, lacked parallel execution capability at the time, which slowed down the merge performance.

Development and Optimization

At the time of the benchmark in 2012, Pandas was a newer library that had been developed in a more modern and optimized way compared to data.table. Pandas was built using the NumPy library, which has a strong focus on performance and optimization. Additionally, Pandas had been developed using Cython, which allowed for more efficient memory management and faster execution. On the other hand, data.table had been developed on top of base R libraries, which are not optimized for performance and lack efficient memory management capabilities.

Conclusion

In conclusion, the faster performance of Pandas merges in 2012 compared to data.table merges in R can be attributed to several factors, including differences in data structures, parallel execution capability, and development and optimization. While data.table has since improved and now offers similar parallel execution capability, Pandas remains a popular choice for data analysis due to its efficient memory management and optimization.
