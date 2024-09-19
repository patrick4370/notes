--- 
title: Vim Plugins
lang: en
---

## preservim/nerdcommenter

Comment functions so powerful — no comment necessary.

To install, add the the Vim Plug Manager

1. Add `Plug 'preservim/nerdcommenter'` to your vimrc file.
2. Reload your vimrc or restart
3. Run `:PlugInstall`

Make sure that `filetype plugin on` is in your `.vimrc`

I have configured the following settings in my `.vimrc` file.

```vim
" Create default mappings
let g:NERDCreateDefaultMappings = 1

" Add spaces after comment delimiters by default
let g:NERDSpaceDelims = 1

" Enable trimming of trailing whitespace when uncommenting
let g:NERDTrimTrailingWhitespace = 1

" Enable NERDCommenterToggle to check all selected lines is commented or not 
let g:NERDToggleCheckAllLines = 1
```
Mappings I Use



