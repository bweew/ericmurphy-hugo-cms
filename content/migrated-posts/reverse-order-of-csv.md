---
title: 'reverse order of csv'
date: 2024-02-25T02:37:00.001-05:00
draft: false
url: /2024/02/reverse-order-of-csv.html
tags: 
- blogposts
---

you can't sort asc/desc like sql and even if you did its probably not what you want. Made that mistake once, sorted all the sentences alphabetically. didn't notice till after I saved rendering it unintelligible.

using tails it prints the last 10 lines of a file but you can use the -n 100 option to show 100 lines.

the -r option reverses it.

```
tail -n 100 data.csv > temp.csv && mv temp.csv data.csv 
```

on a-shell mini its not letting me pipe it into a temp file so im just going to make a new one called rev-data.csv

Why?  
my "sharelinks page" where the links are dynamically generated from a csv is starting to get long. I changed my mind, now I want the new links at the top.