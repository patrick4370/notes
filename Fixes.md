---
title: Vim Fixes
lang: en
---

I had a problem in vim where the <kbd>HOME</kbd> and <kbd>END</kbd> keys would
insert a new line above the current line and add a H for home and an E for end.
To solve this, I add the following snippet to my `.vimrc` file.

`set term=xterm-256color`

[Vim Editor](Vim_Editor.md)
