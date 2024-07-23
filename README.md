# vim-config


" vim: syntax=vim
https://github.com/clarkt3/vim-config.git

" Enable syntax highlighting and file type detection
syntax on
filetype plugin indent on

" Set Line Number
set number

" Set Spell Check
set spell
set spelllang=en_us

" Set color scheme
colorscheme gruvbox

" Use 4 spaces for Python files
autocmd FileType python setlocal shiftwidth=4 tabstop=4 expandtab

" Specify a directory for plugins
" - Avoid using standard Vim directory names like 'plugin'
call plug#begin('~/.vim/plugged')

" Declare the list of plugins
Plug 'davidhalter/jedi-vim' " Python autocompletion

" Initialize plugin system
call plug#end()

" Enable jedi-vim for Python autocompletion
let g:jedi#completions_enabled = 1

" Additional settings to enhance autocompletion
let g:jedi#completions_command = "<C-Space>"

" Enable debug logging for jedi-vim
let g:jedi#logging = 'debug'

" Basic Enhancements
set nonumber
syntax on
set relativenumber
set showmatch
set autoindent
set smartindent
set wrap
set mouse=a

" Advanced Enhancements
set cursorline
set undofile
set undodir=~/.vim/undodir
set clipboard=unnamedplus
set incsearch
set ignorecase
set smartcase
set showcmd
set ruler
set tabstop=4
set shiftwidth=4
set expandtab

" Mappings and Shortcuts
nnoremap <leader>w :w<CR>
nnoremap <leader>q :q<CR>
nnoremap <leader>wq :wq<CR>
nnoremap <leader>n :NERDTreeToggle<CR>
nnoremap <leader>ln :set invnumber<CR>
nnoremap <leader>c :Commentary<CR>
nnoremap <leader>bn :bnext<CR>
nnoremap <leader>bp :bprevious<CR>

" Plugin Management
execute pathogen#infect()
Plug 'preservim/nerdtree'
Plug 'vim-airline/vim-airline'
Plug 'tpope/vim-fugitive'
Plug 'tpope/vim-commentary'

" Install vim plug manager
call plug#begin('~/.vim/plugged')
Plug 'jiangmiao/auto-pairs'
call plug#end()

" Initialize Vim-Plug
call plug#begin('~/.vim/plugged')

" Add coc.nvim plugin
Plug 'neoclide/coc.nvim', {'branch': 'release'}

" End Vim-Plug initialization
call plug#end()

" Use coc.nvim for auto-completion
" Enable Python support
autocmd FileType python setlocal omnifunc=v:lua.vim.lsp.omnifunc

" Use <Tab> and <Shift-Tab> to navigate through popup menu
inoremap <silent><expr> <Tab> pumvisible() ? "\<C-n>" : "\<Tab>"
inoremap <silent><expr> <S-Tab> pumvisible() ? "\<C-p>" : "\<S-Tab>"

" Trigger completion with <Tab>
inoremap <silent><expr> <Tab> pumvisible() ? "\<C-n>" : "\<Tab>"
inoremap <silent><expr> <S-Tab> pumvisible() ? "\<C-p>" : "\<S-Tab>"

" Set completeopt to have a better completion experience
set completeopt=menuone,noinsert,noselect
