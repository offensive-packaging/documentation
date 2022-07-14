---
Title: creddump7
Homepage: https://github.com/Neohapsis/creddump7
Repository: https://gitlab.com/kalilinux/packages/creddump7
Architectures: all
Version: 0.1+git20190429-0kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### creddump7
 
  This package contains a Python tool to extract various credentials and
  secrets from Windows registry hives.
  It's based on the creddump program. Many patches and fixes have been applied
  by Ronnie Flathers.
 
 **Installed size:** `78 KB`  
 **How to install:** `sudo apt install creddump7`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 * python3-pycryptodome
 {{< /spoiler >}}
 
 ##### creddump7
 
 
 ```
 root@kali:~# creddump7 -h
 
 > creddump7 ~ Python tool to extract credentials and secrets from Windows registry hives
 
 /usr/share/creddump7
 |-- __pycache__
 |-- cachedump.py
 |-- framework
 |-- lsadump.py
 `-- pwdump.py
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
