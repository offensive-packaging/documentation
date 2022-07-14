---
Title: juice-shop
Homepage: https://github.com/juice-shop/juice-shop
Repository: https://gitlab.com/kalilinux/packages/juice-shop
Architectures: amd64
Version: 14.0.0-0kali1
Metapackages: kali-linux-labs 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### juice-shop
 
  This package contains a modern and sophisticated insecure web application! It
  can be used in security trainings, awareness demos, CTFs and as a guinea pig
  for security tools! Juice Shop encompasses vulnerabilities from the entire
  OWASP Top Ten along with many other security flaws found in real-world
  applications!
   
  WARNING: Do not upload it to your hosting provider's public html folder or any
  Internet facing servers, as they will be compromised.
 
 **Installed size:** `307.54 MB`  
 **How to install:** `sudo apt install juice-shop`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * nodejs 
 * npm
 {{< /spoiler >}}
 
 ##### juice-shop
 
 
 ```
 root@kali:~# juice-shop -h
 [*] Please wait for the Juice-shop service to start.
 [*]
 [*] You might need to refresh your browser once it opens.
 [*]
 [*]  Web UI: http://127.0.0.1:42000
 
 ```
 
 - - -
 
 ##### juice-shop-stop
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
