---
title: 'how to copy a range of lines '
date: 2024-02-14T22:25:00.001-05:00
draft: false
url: /2024/02/how-to-copy-range-of-lines.html
tags: 
- vim
---

let's say youve got an epub of some book  
you use calibre to convert it to .txt  
so you can practise typing a chapter of it.  
you can skim through the toc

*   use / to search for chapter headings
*   or you can visual selct a a word with viw  
    then use \* and # to nav to next and prev instance

* * *

to copy a range to system clipboard:  
:1,10y +  
this copies line 1 to line 10 to the "+y system clipboard

* * *

*   you could also use :grep or :vimgrep but im not going to get into it this time
*   gf = go to file
*   gd = go to definition
*   ctrl \[ on visual selection is the same as gd?