set scrolloff=10
set number
set rnu " relative number
set tabstop=2 softtabstop=2
set shiftwidth=2
set expandtab
set autoindent
set smartindent
set termguicolors
" set guicursor=
" set nohlsearch
" set hidden
" set noerrorbells
" set nu
" set nowrap
" set noswapfile
" set nobackup
" set undodir=~/.vim/undodir
" set undofile
" set incsearch

" start vim plug script https://github.com/junegunn/vim-plug
call plug#begin('~/.vim/plugged')
" install fzf https://github.com/junegunn/fzf.vim
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
Plug 'junegunn/fzf.vim'
" install color scheme
Plug 'ayu-theme/ayu-vim'
Plug 'preservim/nerdtree'
" end vim plug script
call plug#end()

" colorscheme koehler
" syntax enable
set termguicolors
let ayucolor = "dark"
colorscheme ayu

let mapleader = " " " Special key that needs to be pressed before running custom commands
" n = normal mode 
" nore = no recursive execution. if there are multiple maps with the same keys, it won't execute all of them
" map = create new map 

" Use NetRw (default navigator on vim) to open explorer
" nnoremap <leader>e :20Vex<CR>
" Use NERDtree explorer
nnoremap <leader>ex :NERDTree<CR> 
nnoremap <leader>eg :NERDTreeVCS<CR> 
nnoremap <leader>ec :NERDTreeClose<CR> 
" reinitialize vimrc with space and enter
nnoremap <leader><CR> :so ~/.vimrc<CR>
" Use space fg to open git files with vim-plug fzf
nnoremap <leader>fg :GFiles<CR>
" Use space to open files with vim-plug fzf
nnoremap <leader>ff :Files<CR>
" Jump down 20 spaces
nnoremap <C-j> 20j
" Jump up 20 spaces
nnoremap <C-k> 20k
" Copy into system clipboard
vnoremap <leader>y "+y
" Copy entire file into system clipboard
nnoremap <leader>Y gg"*yG
" Move code down and maintain indentation
vnoremap J :m '>+1<CR>gv=gv
" Move code up and maintain indentation
vnoremap K :m '<-2<CR>gv=gv

" Toggling paste mode to prevent autoindent / comments
" https://dev.to/andy4thehuynh/create-a-shortcut-to-toggle-paste-mode-with-vim-5205#:~:text=Toggle%20on%20paste%20mode%3A%20hit,paste%20mode%3A%20%5C%20%2B%20P%20.
nnoremap <leader>i :set paste!<CR>

