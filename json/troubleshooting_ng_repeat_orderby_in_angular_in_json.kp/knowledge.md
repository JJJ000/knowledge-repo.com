---
title: Troubleshooting 'ng-repeat orderby' in angular
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: ng-repeat orderBy requires an array of objects, not a JSON object.
---

**Contents**

[TOC]

## Section 1: Overview

Angular's `ng-repeat` directive is a powerful tool for displaying data from a JSON file. It allows you to iterate over a collection of data and display it in a structured way. However, it can be difficult to make `ng-repeat` work with JSON data, especially when trying to order the data in a specific way.

## Section 2: The Problem

The problem with using `ng-repeat` with JSON data is that it does not natively support sorting the data. This means that if you want to order your data in a specific way, you must manually sort the data before it is displayed. This can be a tedious and time-consuming process, especially if the data is large or complex.

## Section 3: Solutions

Fortunately, there are several solutions to this problem. One option is to use the `orderBy` filter provided by Angular. This filter allows you to specify a sorting criteria and will automatically sort the data according to that criteria. Another option is to use a library such as Lodash, which provides a wide range of sorting functions that can be used with `ng-repeat`.

## Section 4: Conclusion

In summary, it can be difficult to make `ng-repeat` work with JSON data, especially when trying to order the data in a specific way. However, there are several solutions to this problem, such as using the `orderBy` filter provided by Angular or using a library such as Lodash. With the right approach, it is possible to make `ng-repeat` work with JSON data.
