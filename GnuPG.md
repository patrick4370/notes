---
title: GnuPGuPG
lang: en
---

# GnuPG Basics

## Generate a Secure key

### Create a GPG master private key

To carry this out, you will need

- 3 or 4 USB drives (reset them with `wipefs`)
- Software to burn an image to USB
- [TailsOS](https://tails.net/) or similar to create an air-gap computer.

Boot into TailsOS. We are now in an OS with no internet.

1. Open a terminal window.
2. Delete the ~/.gnupg/ directory with `rm -r ~/.gnupg/`
3. Delete anything on the Desktop directory with `rm Desktop/*`
4. Create a directory in Desktop called `Desktop/my_keys` with `mkdir -p
   Desktop/my_keys`. This is where we will store any data concerning out
   keys.
5. We will firstly generate a password for the master key. `Openssl rand -base64 24 > Desktop/my_keys/password.txt`
6. Copy the password to the clipboard. `cat Desktop/my_keys/password.txt`. Right click and copy.
7. Create the master key with certifying capabilities only. `gpp --expert --full-generate-key`. 
  
  gpg (GnuPG) 2.2.9; Copyright (C) 2018 Free Software Foundation, Inc.
  This is free software: you are free to change and redistribute it.
  There is NO WARRANTY, to the extent permitted by law.

  Please select what kind of key you want:
  (1) RSA and RSA (default)
  (2) DSA and Elgamal
  (3) DSA (sign only)
  (4) RSA (sign only)
  (7) DSA (set your own capabilities)
  **(8) RSA (set your own capabilities)**
  (9) ECC and ECC
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (13) Existing key
  **Your selection? 8** 

**Disable sign capability (type S)**

  Possible actions for a RSA key: Sign Certify Encrypt Authenticate
  Current allowed actions: **Sign Certify Encrypt**

  **(S) Toggle the sign capability**
  (E) Toggle the encrypt capability
  (A) Toggle the authenticate capability
  (Q) Finished

  **Your selection? S**
  
**Disable encrypt capabilities (type E)**

  Possible actions for a RSA key: Sign Certify Encrypt Authenticate
  **Current allowed actions: Certify Encrypt**

  (S) Toggle the sign capability
  **(E) Toggle the encrypt capability**
  (A) Toggle the authenticate capability
  (Q) Finished

  **Your selection? E**
  
**Quit and continue the creation process (type Q)**

  Possible actions for a RSA key: Sign Certify Encrypt Authenticate
  **Current allowed actions: Certify**

  (S) Toggle the sign capability
  (E) Toggle the encrypt capability
  (A) Toggle the authenticate capability
  **(Q) Finished**

  **Your selection? Q**

**Input the desired key size of the master key**

  RSA keys may be between 1024 and 4096 bits long.
  **What keysize do you want? (2048) 4096**
  Requested keysize is 4096 bits

**Setup the expiration for the master key**

  Please specify how long the key should be valid.
        **0 = key does not expire**
        <n>  = key expires in n days
        <n>w = key expires in n weeks
        <n>m = key expires in n months
        <n>y = key expires in n years
  **Key is valid for? (0) 0**
  Key does not expire at all
  Is this correct? (y/N) y

**Construct your user ID (input your full name and email, leave comment empty). Type O to complete**

  GnuPG needs to construct a user ID to identify your key.

  **Real name: <Name>**
  **Email address: <Email>**
  Comment:
  You selected this USER-ID:
  "<Name> <Email>"

  **Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O**

You will be asked for a password. Paste the one in the clipboard.

**Enter a passphrase for your master key**

  ┌──────────────────────────────────────────────────────┐
  │ Please enter the passphrase to                       │
  │ protect your new key                                 │
  │                                                      │
  │ Passphrase: ________________________________________ │
  │                                                      │
  │       <OK>                              <Cancel>     │
  └──────────────────────────────────────────────────────┘

If you did the above steps correctly you should have the following result

  We need to generate a lot of random bytes. It is a good idea to perform
  some other action (type on the keyboard, move the mouse, utilize the
  disks) during the prime generation; this gives the random number
  generator a better chance to gain enough entropy.
  gpg: key 4EF9EF4CDBD7AB1B marked as ultimately trusted
  gpg: revocation certificate stored as '/home/<user>/.gnupg/openpgp-revocs.d/F8DD1C85581AB87675EF97444EF9EF4CDBD7AB1B.rev'
  public and secret key created and signed.

  pub   rsa4096 2018-07-27 **[C]** [expires: 2019-07-27]
        F8DD1C85581AB87675EF97444EF9EF4CDBD7AB1B
  uid                      <Name> <Email>

Store the revocation certificate (created by gpg) for your master key on a physical device.

The key will be generated showing it is a certifying key only.
