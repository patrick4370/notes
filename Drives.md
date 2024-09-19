---
title: Drives
lang: en
---
# Encrypted Drives

## Prepare Drive

To setup a drive for LUKS (Linux Unified Key System) run the following command

`cryptsetup luksFormat /dev/sdXn`

Where

* X is the drive letter
* n is the partition

This is equivalent to 

`sudo cryptsetup --verbose --verify-passphrase --cipher=aes-xts-plain64 --key-size=512 --hash=sha512 --iter-time=5000 --use-random --type luks2 luksFormat /dev/sdXn`

> For an explanation of the options, refer to this [article](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Encryption_options)

## 
