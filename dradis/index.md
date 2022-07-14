---
Title: dradis
Homepage: https://dradisframework.org
Repository: https://gitlab.com/kalilinux/packages/dradis
Architectures: amd64
Version: 4.3.0-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-reporting 
Icon: images/dradis-logo.svg
PackagesInfo: |
 ### dradis
 
  Dradis is a tool to help in the process of penetration testing. Penetration
  testing is about information:
   
   1. Information discovery
   2. Exploit useful information
   3. Report the findings
   
  But penetration testing is also about sharing the information you and your
  teammates gather. Not sharing the information available in an effective way
  will result in exploitation oportunities lost and the overlapping of efforts.
 
 **Installed size:** `576.08 MB`  
 **How to install:** `sudo apt install dradis`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * bundler
 * git
 * libc6 
 * libgcc-s1 
 * libpq5 
 * libruby2.7 
 * libsqlite3-0 
 * libstdc++6 
 * lsof
 * pwgen
 * ruby2.7
 {{< /spoiler >}}
 
 ##### dradis
 
 
 ```
 root@kali:~# dradis -h
 [*] Please wait for the Dradis service to start.
 [*]
 [*] You might need to refresh your browser once it opens.
 [*]
 [*]  Web UI: http://127.0.0.1:3000
 
 ```
 
 - - -
 
 ##### dradis-stop
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
service dradis start
```

![dradis](images/dradis.png)
