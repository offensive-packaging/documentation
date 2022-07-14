---
Title: lapsdumper
Homepage: https://github.com/n00py/LAPSDumper
Repository: https://gitlab.com/kalilinux/packages/lapsdumper
Architectures: all
Version: 0+git20220412-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### lapsdumper
 
  A tool that dumps every LAPS password the account
  has the ability to read with a domain.
 
 **Installed size:** `14 KB`  
 **How to install:** `sudo apt install lapsdumper`  
 
 {{< spoiler "Dependencies:" >}}
 * python3-ldap3
 {{< /spoiler >}}
 
 ##### lapsdumper
 
 
 ```
 root@kali:~# lapsdumper -h
 usage: lapsdumper [-h] -u USERNAME -p PASSWORD [-l LDAPSERVER] -d DOMAIN
 
 Dump LAPS Passwords
 
 options:
   -h, --help            show this help message and exit
   -u USERNAME, --username USERNAME
                         username for LDAP
   -p PASSWORD, --password PASSWORD
                         password for LDAP (or LM:NT hash)
   -l LDAPSERVER, --ldapserver LDAPSERVER
                         LDAP server (or domain)
   -d DOMAIN, --domain DOMAIN
                         Domain
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
