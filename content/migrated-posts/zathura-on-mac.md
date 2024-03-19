---
title: 'Zathura on mac'
date: 2024-01-04T07:58:00.001-05:00
draft: false
url: /2024/01/zathura-on-mac.html
---

I like Zathura on linux mint for opening pdfs because it can navigate with vim bindings. I was having trouble with installing it on mac with homebrew. You think it would be one command like brew install zathura, but you also need mupdf and poppler.

after I got it installed it i couldn't just search for it in the apps to run it Its installed in the homebrew area for some reason I never became aquainted with the file path. Even though i could easily look it up and remember where it saves I for some reason instead choose to forget it. maybe writing about it will help me remember?

my workaround
-------------

I made a fzf one liner to search for stuff and open it

```
 `find /Users/bweew/Documents -type f -iname '*Jon Duckett*' | fzf | xargs -I {} zathura "{}"` 

```