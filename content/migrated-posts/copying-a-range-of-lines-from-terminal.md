---
title: 'copying a range of lines from terminal'
date: 2024-02-17T17:03:00.000-05:00
draft: false
url: /2024/02/copying-range-of-lines-from-terminal.html
tags: 
- terminal
---

 previously posted a way

which involved opening it in vim.

This uses sed instead.

sed -n '246,$p' filename.txt | pbcopy

this copys from line 246 to the end of the file