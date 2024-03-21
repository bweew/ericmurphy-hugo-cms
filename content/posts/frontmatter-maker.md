---
draft: false
date: '2023-12-15 02:05:29'
title: "FrontHugo"
description: "frontmatter maker for hugo using vimscript"
slug: "fronthugo"
authors: []
tags: []
categories: []
---

# Frontmatter maker
some vimscript to make making hugo blogging easier.
add this to your .vimrc then run it with leader f h
(frontmatter hugo)

```
" Function to insert Hugo front matter
function! InsertHugoFrontMatter()
    let front_matter = "+++\n"
    let front_matter .= "draft = false\n"
    let front_matter .= "date = '" . strftime("%Y-%m-%d %H:%M:%S") . "'\n"
    let front_matter .= "title = \"\"\n"
    let front_matter .= "description = \"\"\n"
    let front_matter .= "slug = \"\"\n"
    let front_matter .= "authors = []\n"
    let front_matter .= "tags = []\n"
    let front_matter .= "categories = []\n"
    let front_matter .= "externalLink = \"\"\n"
    let front_matter .= "+++\n\n"

    " Move to the beginning of the file and insert the front matter
    call cursor(1, 1)
    call append(0, split(front_matter, "\n"))
endfunction

" Mapping to trigger the insertion of Hugo front matter
nnoremap <leader>fh :call InsertHugoFrontMatter()<CR>
```

