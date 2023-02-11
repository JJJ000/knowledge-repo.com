---
title: What is the process for automatically formatting JSON when saving in vim?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Install the vim-json plugin and add the following line to your .vimrc file autocmd FileType JSON setl formatprg=json\_reformat\ -i\ 4
---

**Contents**

[TOC]

**Section 1: Install the JSON Syntax Plugin**

1. Download the [vim-json](https://github.com/elzr/vim-json) plugin from GitHub.

2. Extract the contents to your `~/.vim` directory.

3. Add the following lines to your `~/.vimrc` file:

```
syntax on
filetype plugin indent on
au BufWritePre *.json :%!python -m json.tool
```

**Section 2: Configure Auto-Formatting**

1. Open your `~/.vimrc` file and add the following line:

```
autocmd BufWritePre *.json :%!python -m json.tool
```

2. Save the file and restart Vim.

**Section 3: Test the Auto-Formatting**

1. Create a file with some invalid JSON, e.g.

```
{
"name": "John Doe"
"age": 42
}
```

2. Save the file.

3. Check if the file has been auto-formatted:

```
{
    "name": "John Doe",
    "age": 42
}
```

**Section 4: Troubleshooting**

If the auto-formatting is not working, make sure that the `vim-json` plugin is installed correctly and that the `au BufWritePre *.json :%!python -m json.tool` line is present in your `~/.vimrc` file.
