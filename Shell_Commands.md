---
title: Shell Commands
lang: en
---

# Shell Commands

### Shell Expansions

I often have a need to change a file name on the fly. More specifically I want
to change the extension of a file. This is where shell expansion comes into
play. I have a script that uses `pandoc` to convert my markdown files to html. Part of the command looks like this.

```sh
for files in *.md; do
    pandoc "$files" -o "${files%.md}".html
done

```
This removes the .md extension of the file and appends .html to the end, thus creating a new file.

---

Every month I download the latest Arch Linux ISO file. It becomes a chore considering the directory structure changes every month.  The Arch Download page has this line `Current Release: 2024.05.01` which shows what date the ISO was uploaded. The directory looks like this `https://mirror.aarnet.edu.au/pub/archlinux/iso/2024.05.01/` for the mirror I use. Rather than going on the Arch Linux Download page and clicking to get to my mirror page to download, I use the following in a script. 

```sh
iso_url=$(curl --silent https://archlinux.org/download/ | htmlq a --attribute href | grep "aarnet")
iso_name="archlinux-x86_64.iso"

curl -L -R -C - "${iso_url}${iso_name}" -o "$HOME/Downloads/${iso_name}"
```
This makes it nice and easy to `curl` the file to your machine without having to lookup the directory each time.

---

[Index](index.md)
