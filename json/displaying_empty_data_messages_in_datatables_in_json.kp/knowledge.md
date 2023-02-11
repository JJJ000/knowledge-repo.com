---
title: What is the best way to display a message when there is no data in a datatable?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Set the `emptyTable` option to display a custom message when the table has no data.
---

**Contents**

[TOC]

1. Prerequisites
- Ensure you have a valid JSON object with empty data

2. Set Empty Message
- Add a "emptyMessage" property to your JSON object
- Set the value of the emptyMessage property to the desired empty data message

3. Initialize Datatable
- Initialize the DataTable with the JSON object
- Set the "language" option to the emptyMessage property defined in the JSON object

4. Display Empty Data Message
- The empty data message should now be displayed in the DataTable when no data is present
