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

 " Install Python Linter ALE

 call plug#begin('~/.vim/plugged')

 " Other plugins...
 Plug 'dense-analysis/ale'

 call plug#end()

 " Enable ALE and set flake8 as linter
 " Enable ALE
 let g:ale_linters = {
 \   'python': ['flake8'],
 \}

 " Show linting errors as you type
 let g:ale_lint_on_text_changed = 'always'
 let g:ale_lint_on_insert_leave = 1

 " Use flake8 for linting
 let g:ale_python_flake8_executable = 'flake8'
 let g:ale_python_flake8_options = '--max-line-length=88'

 " Install Vim autosave feature
 call plug#begin('~/.vim/plugged')
 Plug '907th/vim-auto-save'
 call plug#end()

 " Enable vim-auto-save
 let g:auto_save = 1

 " Set the interval for autosave (in milliseconds)
 let g:auto_save_interval = 1000

 " Show a message when the file is autosaved
 let g:auto_save_echo_message = 1


 " call plug#begin('~/.vim/plugged')
 " Plug '907th/vim-auto-save'
 " call plug#end()

 " Enable vim-auto-save
 " let g:auto_save = 1

 " Set the interval for autosave (in milliseconds)
 " let g:auto_save_interval = 1000

 " Show a message when the file is autosaved
 "let g:auto_save_echo_message = 1

 " Additional Customizations
 " Disable autosave in insert mode
 " let g:auto_save_in_insert_mode = 0

 " Enable autosave only for Python files
 " autocmd FileType python let g:auto_save = 1

 " Disable autosave for Markdown files
 " autocmd FileType markdown let g:auto_save = 0
