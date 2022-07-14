---
Title: wifipumpkin3
Homepage: https://github.com/P0cL4bs/wifipumpkin3
Repository: https://gitlab.com/kalilinux/packages/wifipumpkin3
Architectures: all
Version: 1.1.2R2-0kali3
Metapackages: 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wifipumpkin3
 
  This package contains a powerful framework for rogue access point attack,
  written in Python, that allow and offer to security researchers, red teamers
  and reverse engineers to mount a wireless network to conduct a
  man-in-the-middle attack.
 
 **Installed size:** `9.27 MB`  
 **How to install:** `sudo apt install wifipumpkin3`  
 
 {{< spoiler "Dependencies:" >}}
 * hostapd
 * iptables
 * iw
 * net-tools
 * python3
 * python3-asn1crypto
 * python3-bs4
 * python3-dhcplib
 * python3-dnslib
 * python3-dnspython
 * python3-flask 
 * python3-flask-restx
 * python3-isc-dhcp-leases
 * python3-jwt
 * python3-loguru
 * python3-markupsafe
 * python3-netaddr
 * python3-netifaces
 * python3-openssl
 * python3-pyqt5
 * python3-pyqt5.sip
 * python3-requests
 * python3-scapy
 * python3-tabulate
 * python3-termcolor
 * python3-twisted
 * python3-urwid
 * python3-werkzeug
 * wireless-tools
 {{< /spoiler >}}
 
 ##### captiveflask
 
 
 ```
 root@kali:~# captiveflask -h
 /usr/bin/captiveflask: 1: from: not found
 /usr/bin/captiveflask: 2: from: not found
 import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
 import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
 import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
 /usr/bin/captiveflask: 10: Syntax error: "(" unexpected
 ```
 
 - - -
 
 ##### sslstrip3
 
 
 ```
 root@kali:~# sslstrip3 -h
 /usr/bin/sslstrip3: 1: sslstrip is a MITM tool that implements Moxie Marlinspike's SSL stripping attacks.: not found
 /usr/bin/sslstrip3: 3: __author__: not found
 /usr/bin/sslstrip3: 4: __email__: not found
 /usr/bin/sslstrip3: 5: __license__: not found
 /usr/bin/sslstrip3: 25: from: not found
 /usr/bin/sslstrip3: 26: from: not found
 /usr/bin/sslstrip3: 28: from: not found
 /usr/bin/sslstrip3: 29: from: not found
 /usr/bin/sslstrip3: 30: from: not found
 /usr/bin/sslstrip3: 31: Syntax error: "(" unexpected
 ```
 
 - - -
 
 ##### wifipumpkin3
 
 
 ```
 root@kali:~# wifipumpkin3 -h
 usage: wifipumpkin3 [-h] [-i INTERFACE] [-s SESSION] [-p PULP] [-x XPULP]
                     [-m WIRELESS_MODE] [--no-colors] [--rest]
                     [--restport RESTPORT] [--username USERNAME]
                     [--password PASSWORD] [-v]
 
 wifipumpkin3 - Powerful framework for rogue access point attack. See:
 https://wifipumpkin3.github.io/docs/getting-started#usage
 
 options:
   -h, --help            show this help message and exit
   -i INTERFACE          set interface for create AP
   -s SESSION            set session for continue attack
   -p PULP, --pulp PULP  interactive sessions can be scripted with .pulp file
   -x XPULP, --xpulp XPULP
                         interactive sessions can be string with ";" as the
                         separator
   -m WIRELESS_MODE, --wireless-mode WIRELESS_MODE
                         set wireless mode settings
   --no-colors           disable terminal colors and effects.
   --rest                Run the Wp3 RESTful API.
   --restport RESTPORT   Port to run the Wp3 RESTful API on. default is 1337
   --username USERNAME   Start the RESTful API with the specified username
                         instead of pulling from wp3.db
   --password PASSWORD   Start the RESTful API with the specified password
                         instead of pulling from wp3.db
   -v, --version         show program's version number and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
