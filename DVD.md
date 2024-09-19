---
title: DVD 
lang: en
---

# DVD

## MakeMKV

I found today (07/June/2024 14:50) that MakeMKV wouldn't start and
displayed the following error. `Cannot mix incompatible Qt library (5.15.2) with this library (5.15.3)`

After a search, I found the solution was to install `qt5-styleplugins`

Problem solved.

An excert of a comment on the AUR page for `qt5-styleplugins` says this ...

> Quick reminder: qt-base 5.15.7+kde+r176-1 has been released; Users of this package will need to rebuild qt5-styleplugins (yay -S --rebuild qt5-styleplugins), otherwise Qt applications will crash.
> 
> The pkgrel of this package has been bumped so this should be done automatically by your AUR helper.

[index](index.md)
