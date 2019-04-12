---
layout: default
---

# Vim for noobs
## session from the April offsite 2019

# &nbsp;

## Install Vim

[Apple's vim](/apple-vim.html)

[Homebrew's vim](/brew-vim.html)

`brew search vim`

```
avimetaedit        
macvim             
neovim             
pacvim             
pyvim              
vim    
vim@7.4            
vimpager           
vimpc
```

`brew info vim`

```
vim: stable 8.1.1100
Vi 'workalike' with many additional features
https://www.vim.org/
From: https://github.com/Homebrew/homebrew-core/blob/master/Formula/vim.rb
Dependencies:
Required: gettext, lua, perl, python, ruby
```
`brew install vim`

# &nbsp;

## Configuring vim

[/usr/local/Cellar/vim/8.1.1100/share/vim/vim81/defaults.vim](https://github.com/vim/vim/blob/master/runtime/defaults.vim)

[/usr/local/Cellar/vim/8.1.1100/share/vim/vim81/vimrc_example.vim](https://github.com/vim/vim/blob/master/runtime/vimrc_example.vim)

[https://github.com/vpetkov/Terminal/blob/master/.vimrc](https://github.com/vpetkov/Terminal/blob/master/.vimrc)

# &nbsp;

## Vim packages

Vim 8 has package support built in.

Vim will load automatically packages (a.k.a. plugins) from:  
`~/.vim/pack/mypack/start/`

And will hold packages that are not loaded automatically in:  
`~/.vim/pack/maypack/opt/`

Those can be loaded using:  
`:packadd packagename`

Adding packages is simple if you keep vim's configuration in git, using submodules:  
`git submodule init`  
`git submodule add git@github.com:packagename .vim/pack/mypack/start/packagename`  
`git commit`

To update/remove packages simply `update` or `deinit` the git module

# &nbsp;

## My packages

```
[submodule ".vim/pack/vpetkov/start/file-line"]
  path = .vim/pack/vpetkov/start/file-line
	url = git@github.com:lervag/file-line.git
[submodule ".vim/pack/vpetkov/start/commentary"]
  path = .vim/pack/vpetkov/start/commentary
	url = git@github.com:tpope/vim-commentary.git
[submodule ".vim/pack/vpetkov/start/rails"]
  path = .vim/pack/vpetkov/start/rails
	url = git@github.com:tpope/vim-rails.git
[submodule ".vim/pack/vpetkov/start/ctrlp"]
  path = .vim/pack/vpetkov/start/ctrlp
	url = git@github.com:ctrlpvim/ctrlp.vim.git
[submodule ".vim/pack/vpetkov/start/vim-completes-me"]
	path = .vim/pack/vpetkov/start/vim-completes-me
	url = git@github.com:ajh17/VimCompletesMe.git
```

[https://github.com/bogado/file-line](https://github.com/bogado/file-line)  
[https://github.com/tpope/vim-commentary](https://github.com/tpope/vim-commentary)  
[https://github.com/tpope/vim-rails](https://github.com/tpope/vim-rails)  
[https://github.com/ctrlpvim/ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)  
[https://github.com/ajh17/VimCompletesMe](https://github.com/ajh17/VimCompletesMe)  

# &nbsp;

## Configuring packages

```

" Remap 'open in current buffer' from RETURN to CTR-B
" I have to tie my hands because cannot control myself

let g:ctrlp_clear_cache_on_exit = 0
let g:ctrlp_prompt_mappings = {
      \ 'AcceptSelection("e")': ['<c-b>'],
      \ }


" Remap from 'gc' because I'm used to '\\'

vmap \\  <Plug>Commentary
nmap \\ <Plug>CommentaryLine
```

# &nbsp;

## How do I know this

Vim FAQ can be found here: [https://vimhelp.org/vim_faq.txt.html](https://vimhelp.org/vim_faq.txt.html)

# &nbsp;
# &nbsp;
# &nbsp;
# &nbsp;
# &nbsp;
