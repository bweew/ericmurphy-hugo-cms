---
title: my vim setup from scratch
date: 2024-07-09T03:04:25.237Z
---
\# install vimplug

curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

```
call plug#begin('~/.vim/plugged')
Plug 'vimwiki/vimwiki'
Plug 'vim-airline/vim-airline'
Plug 'matze/vim-move'
Plug 'jceb/vim-orgmode'
Plug 'tpope/vim-speeddating'
Plug 'vim-scripts/utl.vim'
Plug 'mattn/calendar-vim'
Plug 'vim-airline/vim-airline-themes'
Plug 'sainnhe/sonokai'
Plug 'morhetz/gruvbox'
Plug 'tpope/vim-fugitive'
Plug 'plasticboy/vim-markdown'
Plug 'sfztools/sfz.vim'
Plug 'ap/vim-css-color'
Plug '907th/vim-auto-save'
Plug 'jiangmiao/auto-pairs'
Plug 'ajorgensen/vim-markdown-toc'
Plug 'mattn/emmet-vim'
Plug 'kshenoy/vim-signature'
Plug 'mechatroner/rainbow_csv'
Plug 'dhruvasagar/vim-table-mode'
Plug 'godlygeek/tabular'
Plug 'scrooloose/nerdtree'
Plug 'junegunn/goyo.vim'
Plug 'reedes/vim-pencil'
call plug#end()

" Enable folding based on Org mode headings
let g:org_special_headline_highlight = 1
let g:org_headline_fold = 1
" Remap vim-move from alt to shift
let g:move_key_modifier_visualmode = 'S'
autocmd FileType css set omnifunc=csscomplete#CompleteCSS
autocmd FileType javascript set omnifunc=javascriptcomplete#CompleteJS
set background=dark
colorscheme sonokai
syntax enable
set nobackup
set nowb
set noswapfile
set autoread
set wildmenu
set ffs=unix,dos,mac
set encoding=utf8
set showmatch
set backspace=eol,start,indent
set autoread
set wrap
set si
set ai
filetype plugin on
filetype indent on
set tabstop=4
set shiftwidth=4
set smarttab
set expandtab
set nocompatible
filetype plugin on
syntax on
set autowriteall
" Automatically save files on change
let g:auto_save = 1
" Set the interval for auto-saving in milliseconds (optional)
let g:auto_save_silent = 1
" Emmet shortcuts
let g:user_emmet_mode='n'
let g:user_emmet_leader_key=','
nnoremap <C-t> :NERDTreeToggle<CR>
" Exit Vim if NERDTree is the only window remaining in the only tab.
autocmd BufEnter * if tabpagenr('$') == 1 && winnr('$') == 1 && exists('b:NERDTree') && b:NERDTree.isTabTree() | quit | endif
nnoremap <C-Right> :bnext<CR>
nnoremap <C-Left> :bprev<CR>
set tags=./tags,tags;/
" Tmux Navigator integration for Vim
let g:navigator_no_mappings = 1
nnoremap <silent><c-h> :TmuxNavigateLeft<cr>
nnoremap <silent><c-j> :TmuxNavigateDown<cr>
nnoremap <silent><c-k> :TmuxNavigateUp<cr>
nnoremap <silent><c-l> :TmuxNavigateRight<cr>
set clipboard=unnamedplus
```