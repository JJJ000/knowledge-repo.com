---
title: Formatting JSON data beautifully in ipython notebook
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: In IPython Notebook, you can use the `json.dumps` command to format JSON data in a more readable format.
---

**Contents**

[TOC]

**Section 1: Install the ipyjson Library**

The ipyjson library can be used to format JSON data in IPython Notebook. To install the library, open a terminal window and type the following command:

`pip install ipyjson`

**Section 2: Import the ipyjson Library**

Once the ipyjson library is installed, it needs to be imported into the IPython Notebook. To do this, type the following command in a cell within the IPython Notebook:

`import ipyjson`

**Section 3: Format the JSON Data**

To format the JSON data, use the ipyjson library's `pprint()` function. This will take the JSON data and format it in a readable, easy-to-understand way. To use the `pprint()` function, type the following command in a cell within the IPython Notebook:

`ipyjson.pprint(data)`

where `data` is the name of the JSON data.

**Section 4: Display the JSON Data**

Once the JSON data is formatted, it can be displayed in the IPython Notebook. To do this, type the following command in a cell within the IPython Notebook:

`print(ipyjson.dumps(data))`

where `data` is the name of the JSON data. This will display the formatted JSON data in the IPython Notebook.
