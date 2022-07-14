---
Title: nasty
Homepage: http://www.vanheusden.com/nasty/
Repository: https://salsa.debian.org/pkg-security-team/nasty
Architectures: any
Version: 0.6-4
Metapackages: kali-linux-everything kali-tools-forensics 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### nasty
 
  Nasty is a program that helps you to recover the passphrase of your PGP or
  GPG-key in case you forget or lost it. The following features will make things
  easier:
   - set minimum/maximum length of the passphrase
   - incremental mode, random mode or reads a file for guessing
   - charset filter
   
  This package is useful in forensics investigations.
 
 **Installed size:** `33 KB`  
 **How to install:** `sudo apt install nasty`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgpgme11 
 {{< /spoiler >}}
 
 ##### nasty
 
 A tool which helps you to recover your GPG passphrase
 
 ```
 root@kali:~# man nasty
 NASTY(1)                         User Commands                        NASTY(1)
 
 NAME
        nasty - A tool which helps you to recover your GPG passphrase
 
 SYNOPSIS
        nasty [OPTIONS]
 
 DESCRIPTION
        nasty is a program that helps you to recover the passphrase of your PGP
        or GPG-key in case you forget or lost it.
 
 OPTIONS
        -a x   set minimum length of passphrase
 
        -b x   set maximum length
 
        -m x   set guessing mode:
                  incremental: try them all
                  random: try at random
                  file: read phrases from file (use -i)
 
        -i x   file to read the passphrases from
 
        -f x   file to write the found passphrase to
 
        -c x...
               charset, one or more from the following:
                  a: a-z
                  A: A-Z
                  0: 0-9
                  .: all ascii values (32...126)
                  +: 32...255 (default(!))
 
        -h     show command options
 
 ISSUES
        Nasty will not work if you try it with a gpg-agent running in your sys-
        tem.  For  obvious reasons the agent will ask you the passphrase to ac-
        cess your private key - which you probably don't record, right? :)
 
 AUTHOR
        This manual page was written by Tiago Bortoletto Vaz <tiago@debian.org>
        for the Debian GNU/Linux system (but may be used by others).
 
 nasty                           September 2009                        NASTY(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
