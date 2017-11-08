# Stupid Vim Tricks

This is a super-short (heh!) list of tools and tricks I use for pushing around
my editor of choice: Vim. It's not exhaustive and it's not exclusive. It's
just a summary of some things that improve my quality of life when working on
lots of code scattered across lots of files and in lots of languages.

## My Plugins

 * **vim-plug** - Plugin Manager
 * **vim-lucius** - The best colorscheme of all time
 * **vim-fugitive** - Git tools
 * **vim-rails** - Rails tools
 * **vim-commentary** - Toggle comments quickly
 * **NERDTree** - File tree browser
 * **fzf** and **fzf.vim** - Wrapper for fzf

## Extra Tools

 * **ag** - The Silver Searcher (`brew install the_silver_searcher`)
 * **fzf** - General-purpose fuzzy finder (brew install fzf)
 * **entr** - File watcher / re-runner
 * `alias ae='ag -l | entr -c'`
 * `alias aer='ag -l | entr -c rspec'`

## Finding Files by Name

 * `:e app/**/*cont<tab>` - built-in
 * `:Files` - find files with fzf, nmap this to something like ctrl-f
 * `:Buffers` - find buffers with fzf, nmap this to something like ctrl-b
 * `:sb pa<tab>` - split window to another buffer (e.g., pages_controller)
 * `:NERDTreeToggle` - open file tree browser, nmap this (I use <Leader>d)

## Finding Files by Contents

 * `:set grepprg=ag` - Use ag for grep from Vim
 * `:grep sidebar.pages` - Search for 'sidebar.pages'
 * `:copen / :cn / :cp / :cclose` - Navigate grep hits
 * `nmap <c-n> :cn<cr>` - Move to the next search hit
 * `nmap <c-p> :cp<cr>` - Move to the previous search hit

## Working with Source

 * `==` - auto-align a line, works with visual line mode
 * `<<` / `>>` - indent or outdent lines
 * `%` - Move to matching brace
 * `ctrl-p` / `ctrl-n` - autocompletion
 * `ci(` / `ci"` - change inside delimiters
 * `gcc` / `[motion]gc` - comment/uncomment some lines
 * `V` / `ctrl-v` - Visual line / visual block
 * `"+y` - Yank to system clipboard

## Integrated Terminal

 * `:terminal` - nmap this to something like <Leader>t
 * `ctrl-w` - / `ctrl_w` + - resize splits
 * combined with ag and entr, auto test runner on save

## Using vim-rails

 * `:Einit[ializer]` - open an initializer (routes.rb by default)
 * `:Eco[ntroller]` - open a controller
 * `:A` / `:AS` / `:AV` - open alternate file (usually specs), optionally in a split 

## Using vim-fugitive

 * `:Gstatus` - Show which files are changed / staged
 * (on status screen) `D` - View file diff
 * `:Gcommit` / `C` (in status split) - Commit and author message in-editor

