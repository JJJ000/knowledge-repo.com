---
title: Sending information to a bootstrap modal
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Pass data to a bootstrap modal by setting the modal`s content to the data using jQuery.
---

**Contents**

[TOC]

## Setting Up the Modal

To pass data to a bootstrap modal, first you must create the modal in HTML. This can be done by adding the `modal` class to a `div` element and adding the attributes `data-toggle="modal"` and `data-target="#modal-id"`. The `#modal-id` should be replaced with the `id` of the modal.

## Passing the Data

Once the modal is set up, the data can be passed to the modal using JavaScript. This can be done by creating a variable to store the data and then passing it to the modal using the `modal('show')` method. The data can then be accessed using the `data` property of the modal.

## Adding Event Listeners

In order to ensure that the data is passed to the modal correctly, event listeners should be added to the modal. This can be done by using the `on()` method to add an event listener to the modal that will be triggered when the modal is opened. This event listener can then be used to set the data on the modal.

## Displaying the Data

Once the data has been passed to the modal, it can be displayed on the modal. This can be done by using the `modal('show')` method to open the modal and then using HTML to display the data. This can be done by using the `data` property of the modal to access the data and then using HTML to display it.
