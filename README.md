GVIM
====

My vim configuration

set nu
set encoding=utf-8
syntax enable
syntax on
colorscheme desert
set autoread
set cursorline
hi cursorline guibg=#0A2B1D "#222222"
hi CursorColumn guibg=#333333
set si
set ai
set nofen
set fdl=0
set ruler
set showmatch
set incsearch
set showcmd
set cindent
set shiftwidth=4
set expandtab
set tabstop=4
set autochdir
set syntax=on
set nowrap
set nocompatible
set mouse=a
set confirm
set fileformat=unix
set clipboard+=unnamed
"自动打开nerdtree"
autocmd VimEnter * NERDTree
let NERDTreeShowBookmarks=1
let NERDTreeChDirMode=2

"隐藏工具栏"
set guioptions-=T
"command-t"
nmap ,t :CommandT<CR>
nmap ,b :CommandTBuffer<CR>

set tags=/var/www/tags,tags

"自动打开taglist"
autocmd VimEnter * TlistToggle
let s:tlist_def_go_settings = 'go;f:func;v:var;t:type' 

let Tlist_Show_One_File=1
let Tlist_Use_Right_Window=1
let Tlist_Compact_Format=1
autocmd FileType php noremap <C-L> :!/usr/local/bin/php -l %<CR>
let Tlist_Exit_OnlyWindow = 1
filetype plugin indent on
"定义快捷键"
noremap<F2> :w!<cr>
noremap<F3> :q!<cr>
noremap<F4> :wq!<cr>
noremap<F8> :!go run /var/www/test/"%"<cr>
"MiniBufExplorer"
let g:miniBufExplMapWindowNavVim = 1 
let g:miniBufExplMapWindowNavArrows = 1 
let g:miniBufExplMapCTabSwitchBufs = 1 
let g:miniBufExplModSelTarget = 1 
