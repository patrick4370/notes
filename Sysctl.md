---
title: SysCtl
lang: en
---

# Sysctl

sysctl is a tool for examining and changing kernel parameters at runtime. sysctl is implemented in procfs, the virtual process file system at /proc

## Allow unrestricted access to dmesg

`# echo "kernel.dmesg_restrict=0" > /etc/sysctl.d/00-dmesg.conf`

## Disable automatic core dumps

`# echo "kernel.core_pattern=|/bin/false" > /etc/sysctl.d/50-coredump.config`

[Arch Fixes](Arch_Fixes.md)
