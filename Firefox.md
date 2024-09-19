--- 
title: Firefox 
lang: en 
---

## Older Version

If you get a "You've launched an older version of Firefox" error message
edit the Thunderbird shortcut to add `-allow-downgrade`. In the future you
will need to use that if you want to use an older version of Thunderbird
with an existing profile. 

## i3wm Container

To keep Firefox within an i3 container in full screen mode, change the
following in `about:config`

`full-screen-api.ignore-widgets` to true

## LibreWolf 

Now using LibreWolf for the extra security. The above commands will work
with LibreWolf as it is a clone of Firefox

## Larger Menu Fonts

You can set layout.css.devPixelsPerPx to 1.0 (default is -1) on the
about:config page. Adjust its value in 0.1 or 0.05 steps (1.1 or 0.9) until
icons or text looks right. 

Modifying layout.css.devPixelsPerPx affects user
interface and web pages (global zoom). You can use an extension to correct
the appearance of web pages. 

[Index](index.md)
