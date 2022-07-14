---
Title: command-not-found
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/command-not-found
Architectures: all
Version: 20.10.1-1+kali2
Metapackages: 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### command-not-found
 
  This package will install a handler for command_not_found that looks up
  programs not currently installed but available from the repositories.
 
 **Installed size:** `103 KB`  
 **How to install:** `sudo apt install command-not-found`  
 
 {{< spoiler "Dependencies:" >}}
 * apt-file 
 * lsb-release
 * python3
 * python3-apt
 {{< /spoiler >}}
 
 ##### command-not-found
 
 
 ```
 root@kali:~# command-not-found -h
 Usage: command-not-found [options] <command-name>
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -d DATA_DIR, --data-dir=DATA_DIR
                         use this path to locate data fields
   --ignore-installed, --ignore-installed
                         ignore local binaries and display the available
                         packages
   --no-failure-msg      don't print '<command-name>: command not found'
 ```
 
 - - -
 
 ##### update-command-not-found
 
 Update the command-not-found cache
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
