---
title: Vim Registers
lang: en
---

## Vim Registers

A vim register allows you to save text for later retrieval. If you go into command 
mode and type `:registers` it will display the registers and their content.

```
 Type Name Content
  c  ""   )
  c  "0   )
  l  "1   rm file.txt &>/dev/null^J
  l  "2   dirs -c >file.txt^J
  l  "3   popd^J
  l  "4   )^J
  l  "5   ^J
  l  "6   cmd_args=(^J
  l  "7   echo $current_dir^J
  l  "8   echo " In wrong directory"^J
  <snip>
```

The registers in vim are

1. The Unnamed Register ""
2. 10 numbered registers "0 to "9
3. The small delete register "-
4. 26 named registers "a to "z or "A to "Z
5. 3 read-only registers ":, "., "%
6. Alternate buffer register "#
7. The expression register "=
8. The selection registers "* and "+
9. The black hole register "_
10. Last search pattern register "/

We can access a register by doing the following

Normal Mode: `"<Register Key>`
Insert Mode: `Ctrl+r <Register Key>`


