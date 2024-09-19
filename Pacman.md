---
title: Pacman
lang: en
---

# Pacman Commands

#### Installing Specific Packages

To install a single package or list of packages, including dependencies, issue the following command: 

`sudo pacman -S package_name1 package_name2 ...`

When there are multiple versions of a packages in different repositories
install for example, install the package from extra like this. 

`sudo pacman -S extra/package`

To install a number of packages sharing similar patterns in their names, one can use curly brace expansion. For example: 

`sudo pacman -S plasma-{desktop,mediacenter,nm}`

#### Installing Package Groups

Some packages belong to a group of packages that can all be installed simultaneously. For example, issuing the command: 

`sudo pacman -S gnome`

To see what packages belong in a group, run:

`pacman -Sg gnome`

#### Removing Packages

To remove a single package, leaving all of its dependencies installed: 

`sudo pacman -R package`

To remove a package and its dependencies which are not required by any other installed package: 

`sudo pacman -Rs package`

::::: Error :::::::::::::::::::::::::::::::::::::::::::
Warning: When removing a group, such as gnome, this ignores the install
reason of the packages in the group, because it acts as though each package
in the group is listed separately. Install reason of dependencies is still
respected. 
:::::::::::::::::::::::::::::::::::::::::::::::::::::::


[Arch Linux](Arch_Linux.md)
