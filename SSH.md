# SSH

## Generate public key from private key

`ssh-keygen -f /path/to/private/key -y`

## Generate key for Yubikey (FIDO)

ssh-keygen -t ed25519-sk -C "patrick@pxe YK1" -O resident -O application=ssh:pxe1 -O verify-required -f ~/.ssh/pxe_ed25519-sk_YK1

## Change private key password

`ssh-keygen -f /path/to/private/key -p`

[Index](index.md)
