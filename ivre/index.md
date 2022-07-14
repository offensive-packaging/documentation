---
Title: ivre
Homepage: https://ivre.rocks
Repository: https://gitlab.com/kalilinux/packages/ivre
Architectures: all
Version: 0.9.16-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ivre
 
  This package contains IVRE (Instrument de veille sur les réseaux extérieurs) or
  DRUNK (Dynamic Recon of UNKnown networks), a network recon framework,
  including tools for passive recon (flow analytics relying on Bro, Argus,
  Nfdump, fingerprint analytics based on Bro and p0f and active recon.
   
  IVRE uses Nmap to run scans, can use ZMap as a pre-scanner; IVRE can also
  import XML output from Nmap and Masscan.
 
 **Installed size:** `21.42 MB`  
 **How to install:** `sudo apt install ivre`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bottle
 * python3-cryptography
 * python3-dbus
 * python3-future
 * python3-matplotlib
 * python3-mysqldb
 * python3-openssl
 * python3-pil
 * python3-psycopg2
 * python3-pymongo
 * python3-sqlalchemy
 * python3-tinydb
 {{< /spoiler >}}
 
 ##### ivre
 
 
 ```
 root@kali:~# ivre -h
 IVRE - Network recon framework
 Copyright 2011 - 2020 Pierre LALET <pierre@droids-corp.org>
 Version 0.9.16
 
 Python 3.10.4 (main, Mar 24 2022, 13:07:27) [GCC 11.2.0]
 
 Linux kali 5.16.0-kali7-amd64 #1 SMP PREEMPT Debian 5.16.18-1kali1 (2022-04-01) x86_64
 
 Dependencies:
     Python module pymongo: 3.11.0
     Python module sqlalchemy: 1.4.31
     Python module psycopg2: 2.9.2 (dt dec pq3 ext lo64)
     Python module cryptography: 3.4.8
     Python module krbV: missing
     Python module PIL: 9.0.1
     Python module MySQLdb: 1.4.6
     Python module dbus: 1.2.18
     Python module matplotlib: 3.5.1
     Python module bottle: 0.12.19
     Python module OpenSSL: 21.0.0
     Python module tinydb: 3.15.2
 
 usage: ivre [COMMAND]
 
 available commands:
   airodump2db
   arp2db
   auditdom
   db2view
   flow2db
   flowcli
   getmoduli
   httpd
   ipcalc
   ipdata
   iphost
   ipinfo
   macinfo
   passiverecon2db
   passivereconworker
   plotdb
   runscans
   runscansagent
   runscansagentdb
   scan2db
   scancli
   scanstatus
   version
   view
   zeek2db
 
 Try ivre help [COMMAND]
 
 ```
 
 - - -
 
 ### ivre-doc
 
  This package contains the documentation for IVRE (Instrument de veille sur les
  réseaux extérieurs) or DRUNK (Dynamic Recon of UNKnown networks), a network
  recon framework, including tools for passive recon (flow analytics relying on
  Bro, Argus, Nfdump, fingerprint analytics based on Bro and p0f and active
  recon.
   
  IVRE uses Nmap to run scans, can use ZMap as a pre-scanner; IVRE
  can also import XML output from Nmap and Masscan.
 
 **Installed size:** `4.91 MB`  
 **How to install:** `sudo apt install ivre-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc 
 * sphinx-rtd-theme-common 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
