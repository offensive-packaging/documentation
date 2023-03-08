---
Title: dradis
Homepage: https://dradisframework.org
Repository: https://gitlab.com/kalilinux/packages/dradis
Architectures: amd64
Version: 4.7.0-0kali1
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
 
 **Installed size:** `576.91 MB`  
 **How to install:** `sudo apt install dradis`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * bundler
 * git
 * libc6 
 * libgcc-s1 
 * libpq5 
 * libruby3.1 
 * libstdc++6 
 * lsof
 * pwgen
 * ruby 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### dradis
 
 
 ```
 root@kali:~# dradis -h
 [i] Something is already using port: 3000/tcp
 COMMAND    PID   USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
 ruby3.1 134319 dradis   13u  IPv6 262115      0t0  TCP localhost:3000 (LISTEN)
 ruby3.1 134319 dradis   14u  IPv4 262116      0t0  TCP localhost:3000 (LISTEN)
 
 UID          PID    PPID  C STIME TTY      STAT   TIME CMD
 dradis    134319       1 33 08:58 ?        Ssl    0:01 /usr/bin/ruby3.1 bin/rails server
 
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
 
 Mar 08 08:58:56 kali bundle[134319]:         /usr/lib/dradis/ruby/3.1.0/gems/railties-6.1.7.2/lib/rails/commands.rb:18:in `<main>'
 Mar 08 08:58:56 kali bundle[134319]:         /usr/lib/dradis/ruby/3.1.0/gems/bootsnap-1.16.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:32:in `require'
 Mar 08 08:58:56 kali bundle[134319]:         /usr/lib/dradis/ruby/3.1.0/gems/bootsnap-1.16.0/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:32:in `require'
 Mar 08 08:58:56 kali bundle[134319]:         bin/rails:5:in `<main>'
 Mar 08 08:58:56 kali bundle[134319]: [2023-03-08 08:58:56] INFO  going to shutdown ...
 Mar 08 08:58:56 kali bundle[134319]: [2023-03-08 08:58:56] INFO  WEBrick::HTTPServer#start done.
 Mar 08 08:58:56 kali bundle[134319]: Exiting
 Mar 08 08:58:56 kali systemd[1]: dradis.service: Deactivated successfully.
 Mar 08 08:58:56 kali systemd[1]: Stopped dradis.service - Dradis web application.
 Mar 08 08:58:56 kali systemd[1]: dradis.service: Consumed 1.715s CPU time.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
service dradis start
```

![dradis](images/dradis.png)
