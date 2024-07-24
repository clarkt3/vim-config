# vim-config

"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

" => General

"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""



syntax on
" filetype plugin indent on

" Set Line Number
set nonumber

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

"Layer these additional setting on later after learning python


" Initialize plugin system


" call plug#end()


" Enable jedi-vim for Python autocompletion


" let g:jedi#completions_enabled = 1


" Additional settings to enhance autocompletion


" let g:jedi#completions_command = "<C-Space>"


" Enable debug logging for jedi-vim


" let g:jedi#logging = 'debug'


" Basic Enhancements


" set nonumber


" syntax on


" set relativenumber


" set showmatch


" set autoindent


" set smartindent


" set wrap


" set mouse=a


" Advanced Enhancements


" set cursorline


" set undofile


" set undodir=~/.vim/undodir


" set clipboard=unnamedplus


" set incsearch


" set ignorecase
