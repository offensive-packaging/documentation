---
Title: juice-shop
Homepage: https://github.com/juice-shop/juice-shop
Repository: https://gitlab.com/kalilinux/packages/juice-shop
Architectures: amd64
Version: 14.0.0+node16-0kali1
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
 
 **Installed size:** `422.46 MB`  
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
 
 
 ```
 root@kali:~# juice-shop-stop -h
 * juice-shop.service - juice-shop web application
      Loaded: loaded (/lib/systemd/system/juice-shop.service; disabled; vendor preset: disabled)
      Active: inactive (dead)
 
 Aug 05 11:08:59 kali npm[1231664]: info: Required file runtime.js is present (OK)
 Aug 05 11:08:59 kali npm[1231664]: (node:1231664) [DEP0152] DeprecationWarning: Custom PerformanceEntry accessors are deprecated. Please use the detail property.
 Aug 05 11:08:59 kali npm[1231664]: (Use `node --trace-deprecation ...` to show where the warning was created)
 Aug 05 11:08:59 kali npm[1231664]: info: Port 42000 is available (OK)
 Aug 05 11:09:03 kali npm[1231664]: info: Server listening on port 42000
 Aug 05 11:09:07 kali systemd[1]: Stopping juice-shop web application...
 Aug 05 11:09:07 kali systemd[1]: juice-shop.service: Killing process 1231695 (node) with signal SIGKILL.
 Aug 05 11:09:07 kali systemd[1]: juice-shop.service: Deactivated successfully.
 Aug 05 11:09:07 kali systemd[1]: Stopped juice-shop web application.
 Aug 05 11:09:07 kali systemd[1]: juice-shop.service: Consumed 4.193s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
