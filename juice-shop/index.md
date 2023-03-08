---
Title: juice-shop
Homepage: https://github.com/juice-shop/juice-shop
Repository: https://gitlab.com/kalilinux/packages/juice-shop
Architectures: amd64
Version: 14.2.0+node18-0kali3
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
 
 **Installed size:** `432.95 MB`  
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
 
 Mar 08 10:28:00 kali npm[3906641]: info: Required file runtime.js is present (OK)
 Mar 08 10:28:00 kali npm[3906641]: info: Required file vendor.js is present (OK)
 Mar 08 10:28:00 kali npm[3906641]: (node:3906641) [DEP0152] DeprecationWarning: Custom PerformanceEntry accessors are deprecated. Please use the detail property.
 Mar 08 10:28:00 kali npm[3906641]: (Use `node --trace-deprecation ...` to show where the warning was created)
 Mar 08 10:28:00 kali npm[3906641]: info: Port 42000 is available (OK)
 Mar 08 10:28:05 kali npm[3906641]: info: Server listening on port 42000
 Mar 08 10:28:13 kali systemd[1]: Stopping juice-shop.service - juice-shop web application...
 Mar 08 10:28:13 kali systemd[1]: juice-shop.service: Deactivated successfully.
 Mar 08 10:28:13 kali systemd[1]: Stopped juice-shop.service - juice-shop web application.
 Mar 08 10:28:13 kali systemd[1]: juice-shop.service: Consumed 4.444s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
