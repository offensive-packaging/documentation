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
 
 Nov 24 05:41:36 kali npm[1143047]: info: Required file main.js is present (OK)
 Nov 24 05:41:36 kali npm[1143047]: info: Required file vendor.js is present (OK)
 Nov 24 05:41:36 kali npm[1143047]: info: Required file polyfills.js is present (OK)
 Nov 24 05:41:36 kali npm[1143047]: (node:1143047) [DEP0152] DeprecationWarning: Custom PerformanceEntry accessors are deprecated. Please use the detail property.
 Nov 24 05:41:36 kali npm[1143047]: (Use `node --trace-deprecation ...` to show where the warning was created)
 Nov 24 05:41:36 kali npm[1143047]: info: Port 42000 is available (OK)
 Nov 24 05:41:40 kali systemd[1]: Stopping juice-shop web application...
 Nov 24 05:41:40 kali systemd[1]: juice-shop.service: Deactivated successfully.
 Nov 24 05:41:40 kali systemd[1]: Stopped juice-shop web application.
 Nov 24 05:41:40 kali systemd[1]: juice-shop.service: Consumed 4.771s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
