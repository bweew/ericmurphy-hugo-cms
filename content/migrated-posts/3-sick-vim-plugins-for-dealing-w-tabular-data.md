---
title: '3 sick vim plugins for dealing w tabular data'
date: 2024-02-12T21:47:00.001-05:00
draft: false
url: /2024/02/3-sick-vim-plugins-for-dealing-w.html
tags: 
- csv
- vim
---

* * *

```
Plug 'dhruvasagar/vim-table-mode'
Plug 'godlygeek/tabular'
Plug 'mechatroner/rainbow_csv'

vimwiki is ok for tables too 
in vimwiki type :VimwikiTable 2 5
(this creates a 2 col 5 row empty table)
move through it with tab and shift tab
and it also auto formats.

item   = 1
flavour        = 2
pistachio              = 3

| align delimiters  | :Tabularize /= |
	* !important note that its not :Tableize 
	* that's table mode, tabularize is for tabular
	
| insert col        | leader tic   |
| delete row        | leader tdd   |
| enable table mode | leader tm    |
| delete column     | leader tdc   |
| add formula       | leader tfa   |
| evaluate formula  | leader tfe   |
| tableize a csv    | leader tt    |

| item      | price |
| hamburger | 1$    |
| hotdog    | 3$    |
|-----------+-------|
| TOTAL     | 4.0   |
/* tmf: $4,2=Sum(1:-1) */

leader tm     = table mode enable
shift v       = visual mode select everything
leader tt     = tablelize a csv
leader tfa    = enter formula Sum(1:-1)
leader tfe    = re-evaluate/re-align table
:Tabularize / = aligns by delimiter

	// and going the oposite way
https://tableconvert.com/markdown-to-csv

(also pretty handy too... 
Plug 'matze/vim-move')
	remapped it from ctrl + jk to shift + jk with ..
" Remap vim-move from alt to shift
let g:move_key_modifier_visualmode = 'S' 
```