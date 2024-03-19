---
title: 'regex to swap 2 columns of a csv'
date: 2024-02-02T10:51:00.000-05:00
draft: false
url: /2024/02/regex-to-swap-2-columns-of-csv.html
tags: 
- regex
- csv
---

cliptools new update with smartfiles is amazing.  
Ive got cliptools running 2 buffers deep.  
enabled global paste in settings for cmd shift c to paste from smart file. my smartfile is {clip:1},{clip:2}(then newline).  
I use this to quickly grab urls and titles to create links for my website.  
my website runs a bunch of javascript that dynamically generates tables with links inside them from the csv.  
By using cliptools I can grab all the links at once and as long as I stay consistant with copying the title,then the link its fine. if they end up backwards, it's not a big deal. Being consistent is the most important because I can easily use a regex to fix it.

### my regex to fix it

```
:%s/\v([^,]+),([^,]+)/\2,\1/g 
```