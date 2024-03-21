+++
draft = false
date = 2023-12-15 01:05:04
title = "Add Date For Hugo In Vim"
slug = "add-date-for-hugo-in-vim"
tags = [] 
categories = []
+++

## Leader D
writing frontmatter sucks.
vim to the resue.

```
" Map <leader>d to insert the current date and time in "YYYY-MM-DD HH:MM:SS" format
nnoremap <leader>d i<C-R>=strftime('%Y-%m-%d %H:%M:%S')<CR><Esc>
```
### vim-hugo-helper
[Plug 'robertbasic/vim-hugo-helper'](https://github.com/robertbasic/vim-hugo-helper)
> its not great but its something
- HugoHelperTitleToSlug
- HugoHelperLink
- HugoHelperDateIsNow
- HugoHelperUndraft
- HugoHelperDraft
