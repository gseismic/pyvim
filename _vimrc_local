"https://segmentfault.com/a/1190000003962806
let mapleader=','
set nocompatible              " required
filetype off                  " required
" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')
" let Vundle manage Vundle, required
Plugin 'gmarik/Vundle.vim'
Plugin 'tmhedberg/SimpylFold'
Plugin 'vim-scripts/indentpython.vim'
Plugin 'nvie/vim-flake8'
"<NERDTREE>
Plugin 'scrooloose/nerdtree'
Plugin 'Xuyuanp/nerdtree-git-plugin'
Plugin 'tiagofumo/vim-nerdtree-syntax-highlight'
"Plug 'jistr/vim-nerdtree-tabs'      " enhance nerdtree's tabs
"Plug 'ryanoasis/vim-devicons'       " add beautiful icons besides files
"Plug 'Xuyuanp/nerdtree-git-plugin'  " display git status within Nerdtree
"Plug 'tiagofumo/vim-nerdtree-syntax-highlight' " enhance devicons
"Plugin 'scrooloose/syntastic'
"Plugin 'jnurmine/Zenburn'
"Plugin 'altercation/vim-colors-solarized'
"Plugin 'jistr/vim-nerdtree'
"Plugin 'preservim/nerdcommenter'
"Bundle 'Valloric/YouCompleteMe'

call vundle#end()            " required

filetype plugin indent on    " required

set splitbelow
set splitright
"split navigations
nnoremap <C-J> <C-W><C-J>
nnoremap <C-K> <C-W><C-K>
nnoremap <C-L> <C-W><C-L>
nnoremap <C-H> <C-W><C-H>

set foldmethod=indent
set foldlevel=99
" Enable folding with the spacebar
nnoremap <space> za

set nu

map tu :tabnew 
map tn :tabnext<cr>
map tp :tabprevious<cr>
map tc :tabclose<cr>

au BufNewFile,BufRead *.py
\ set tabstop=4 |
\ set softtabstop=4 |
\ set shiftwidth=4 |
\ set textwidth=79 |
\ set expandtab |
\ set autoindent |
\ set fileformat=unix |

au BufNewFile,BufRead *.js, *.html, *.css
\ set tabstop=2 |
\ set softtabstop=2 |
\ set shiftwidth=2 |

"https://www.cnblogs.com/yinble/archive/2013/04/02/2995590.html
set tabstop=4
set shiftwidth=4
set expandtab
set cindent

syntax on

"au BufRead,BufNewFile *.py,*.pyw,*.c,*.h match BadWhitespace /\s\+$/
set encoding=utf-8
set hlsearch
map <F4> <leader>ci <CR>

"安装完成后，插件自带的设置效果就很好，但是我们还可以进行一些小的调整：
"let g:ycm_autoclose_preview_window_after_completion=1
"map <leader>g  :YcmCompleter GoToDefinitionElseDeclaration<CR>

"if has('gui_running')
"       	set background=dark
"       	colorscheme solarized
"else
"       	colorscheme zenburn
"endif
"call togglebg#map("<F5>")
"
imap <F2>t <C-r>=strftime("%Y-%m-%d %H:%M:%S")<cr>
map <F2>t i<C-r>=strftime("%Y-%m-%d %H:%M:%S")<cr>

"remember last update or view postion"
" Only do this part when compiled with support for autocommands
if has("autocmd")
" In text files, always limit the width of text to 78 characters
autocmd BufRead *.txt set tw=78
" When editing a file, always jump to the last cursor position
autocmd BufReadPost *
\ if line("'\"") > 0 && line ("'\"") <= line("$") |
\ exe "normal g'\"" |
\ endif
endif


"nerdtree
let g:NERDTreeIndicatorMapCustom = {
    \ "Modified"  : "✹",
    \ "Staged"    : "✚",
    \ "Untracked" : "✭",
    \ "Renamed"   : "➜",
    \ "Unmerged"  : "═",
    \ "Deleted"   : "✖",
    \ "Dirty"     : "✗",
    \ "Clean"     : "✔︎",
    \ 'Ignored'   : '☒',
    \ "Unknown"   : "?"
    \ }

"autocmd vimenter * NERDTree  "自动开启Nerdtree
"let g:NERDTreeWinSize = 25 "设定 NERDTree 视窗大小
"开启/关闭nerdtree快捷键
map <C-f> :NERDTreeToggle<CR>
"let NERDTreeShowBookmarks=1  " 开启Nerdtree时自动显示Bookmarks
"打开vim时如果没有文件自动打开NERDTree
autocmd vimenter * if !argc()|NERDTree|endif
"当NERDTree为剩下的唯一窗口时自动关闭
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTree") && b:NERDTree.isTabTree()) | q | endif
"设置树的显示图标
let g:NERDTreeDirArrowExpandable = '▸'
let g:NERDTreeDirArrowCollapsible = '▾'
"let g:NERDTreeShowLineNumbers=1  " 是否显示行号
let g:NERDTreeHidden=0     "不显示隐藏文件
"Making it prettier
let NERDTreeMinimalUI = 1
let NERDTreeDirArrows = 1
" 不显示隐藏文件
let g:NERDTreeHidden=0
" 过滤: 所有指定文件和文件夹不显示
let NERDTreeIgnore = ['\.pyc$', '\.swp', '\.swo', '\.vscode', '__pycache__']
"F2开启和关闭树"
map <leader>t :NERDTreeToggle<CR>
let NERDTreeChDirMode=1
""显示书签"
let NERDTreeShowBookmarks=1
"设置忽略文件类型"
let NERDTreeIgnore=['\.o$', '\~$', '\.pyc$', '\.swp$']
""窗口大小"
let NERDTreeWinSize=35
"缩进指示线"
let g:indentLine_char='┆'
let g:indentLine_enabled = 1
""autopep8设置"
let g:autopep8_disable_show_diff=1
