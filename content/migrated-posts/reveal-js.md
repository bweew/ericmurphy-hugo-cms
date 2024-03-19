---
title: 'reveal js'
date: 2024-02-22T01:23:00.000-05:00
draft: false
url: /2024/02/reveal-js.html
---

saw a video of a woman who made 175 instagram quote pictures generated using canva's csv to image.  
but unfortunately when I went to try it they have since made it 30 day trial only.

so that got me looking for alternatives,  
imagemagick was one but the text was overflowing.  
could'nt figure out how to get it to wrap or scale.

in reveal js, under examples/layouthelpers.html  
to get text to fit you give it the class "r-fit-text".  
each slide is inside a section tag  
and you would write it just like regular html

ive got my darkreader extension on so i dont need to mess with section data-background="#00ffff" to style the background color