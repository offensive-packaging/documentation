---
Title: juice-shop
Homepage: https://github.com/juice-shop/juice-shop
Repository: https://gitlab.com/kalilinux/packages/juice-shop
Architectures: amd64
Version: 14.5.1+node18-0kali1
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
 
 **Installed size:** `430.63 MB`  
 **How to install:** `sudo apt install juice-shop`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * lsof
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
 
 
 ```
 root@kali:~# juice-shop-stop -h
 * juice-shop.service - juice-shop web application
      Loaded: loaded (/lib/systemd/system/juice-shop.service; disabled; preset: disabled)
      Active: inactive (dead)
 
 May 17 05:21:35 kali npm[991969]: info: Required file tutorial.js is present (OK)
 May 17 05:21:35 kali npm[991969]: info: Required file polyfills.js is present (OK)
 May 17 05:21:35 kali npm[991969]: info: Required file runtime.js is present (OK)
 May 17 05:21:35 kali npm[991969]: info: Required file vendor.js is present (OK)
 May 17 05:21:35 kali npm[991969]: info: Port 42000 is available (OK)
 May 17 05:21:40 kali npm[991969]: info: Server listening on port 42000
 May 17 05:21:45 kali systemd[1]: Stopping juice-shop.service - juice-shop web application...
 May 17 05:21:46 kali systemd[1]: juice-shop.service: Deactivated successfully.
 May 17 05:21:46 kali systemd[1]: Stopped juice-shop.service - juice-shop web application.
 May 17 05:21:46 kali systemd[1]: juice-shop.service: Consumed 5.678s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
