---
Title: dradis
Homepage: https://dradisframework.org
Repository: https://gitlab.com/kalilinux/packages/dradis
Architectures: amd64
Version: 4.5.0-0kali1
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
 
 **Installed size:** `570.67 MB`  
 **How to install:** `sudo apt install dradis`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * bundler
 * git
 * libc6 
 * libgcc-s1 
 * libpq5 
 * libruby3.0 
 * libsqlite3-0 
 * libstdc++6 
 * lsof
 * pwgen
 * ruby 
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
      Loaded: loaded (/lib/systemd/system/dradis.service; disabled; preset: disabled)
      Active: inactive (dead)
 
 Nov 24 04:49:54 kali bundle[85676]:         /usr/lib/dradis/ruby/3.0.0/gems/railties-6.1.6.1/lib/rails/commands.rb:18:in `<main>'
 Nov 24 04:49:54 kali bundle[85676]:         /usr/lib/dradis/ruby/3.0.0/gems/bootsnap-1.13.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:32:in `require'
 Nov 24 04:49:54 kali bundle[85676]:         /usr/lib/dradis/ruby/3.0.0/gems/bootsnap-1.13.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:32:in `require'
 Nov 24 04:49:54 kali bundle[85676]:         bin/rails:5:in `<main>'
 Nov 24 04:49:54 kali bundle[85676]: [2022-11-24 04:49:54] INFO  going to shutdown ...
 Nov 24 04:49:54 kali bundle[85676]: [2022-11-24 04:49:54] INFO  WEBrick::HTTPServer#start done.
 Nov 24 04:49:54 kali bundle[85676]: Exiting
 Nov 24 04:49:54 kali systemd[1]: dradis.service: Deactivated successfully.
 Nov 24 04:49:54 kali systemd[1]: Stopped Dradis web application.
 Nov 24 04:49:54 kali systemd[1]: dradis.service: Consumed 1.692s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
service dradis start
```

![dradis](images/dradis.png)
