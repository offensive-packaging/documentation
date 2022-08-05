---
Title: dradis
Homepage: https://dradisframework.org
Repository: https://gitlab.com/kalilinux/packages/dradis
Architectures: amd64
Version: 4.4.0-0kali1
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
 
 **Installed size:** `576.04 MB`  
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
 
 
 ```
 root@kali:~# dradis-stop -h
 * dradis.service - Dradis web application
      Loaded: loaded (/lib/systemd/system/dradis.service; disabled; vendor preset: disabled)
      Active: inactive (dead)
 
 Aug 05 10:07:22 kali bundle2.7[85803]:         /usr/lib/dradis/ruby/2.7.0/gems/railties-6.1.5.1/lib/rails/commands.rb:18:in `<main>'
 Aug 05 10:07:22 kali bundle2.7[85803]:         /usr/lib/dradis/ruby/2.7.0/gems/bootsnap-1.12.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:30:in `require'
 Aug 05 10:07:22 kali bundle2.7[85803]:         /usr/lib/dradis/ruby/2.7.0/gems/bootsnap-1.12.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:30:in `require'
 Aug 05 10:07:22 kali bundle2.7[85803]:         bin/rails:5:in `<main>'
 Aug 05 10:07:22 kali bundle2.7[85803]: [2022-08-05 10:07:22] INFO  going to shutdown ...
 Aug 05 10:07:22 kali bundle2.7[85803]: [2022-08-05 10:07:22] INFO  WEBrick::HTTPServer#start done.
 Aug 05 10:07:22 kali bundle2.7[85803]: Exiting
 Aug 05 10:07:22 kali systemd[1]: dradis.service: Deactivated successfully.
 Aug 05 10:07:22 kali systemd[1]: Stopped Dradis web application.
 Aug 05 10:07:22 kali systemd[1]: dradis.service: Consumed 1.529s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
service dradis start
```

![dradis](images/dradis.png)
