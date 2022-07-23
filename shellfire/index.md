---
Title: shellfire
Homepage: https://github.com/unix-ninja/shellfire
Repository: https://gitlab.com/kalilinux/packages/shellfire
Architectures: all
Version: 0.4+git20201008-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### shellfire
 
  This package contains an exploitation shell which focuses on exploiting LFI,
  RFI, and command injection vulnerabilities.
 
 **Installed size:** `26 KB`  
 **How to install:** `sudo apt install shellfire`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 {{< /spoiler >}}
 
 ##### shellfire
 
 
 ```
 root@kali:~# shellfire -h
 usage: shellfire [-h] [-d]
 
 Exploitation shell for LFI/RFI and command injection
 
 options:
   -h, --help  show this help message and exit
   -d          enable debugging (show queries during execution)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
