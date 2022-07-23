---
Title: wifipumpkin3
Homepage: https://github.com/P0cL4bs/wifipumpkin3
Repository: https://gitlab.com/kalilinux/packages/wifipumpkin3
Architectures: all
Version: 1.1.3-R3-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wifipumpkin3
 
  This package contains a powerful framework for rogue access point attack,
  written in Python, that allow and offer to security researchers, red teamers
  and reverse engineers to mount a wireless network to conduct a
  man-in-the-middle attack.
 
 **Installed size:** `17.89 MB`  
 **How to install:** `sudo apt install wifipumpkin3`  
 
 {{< spoiler "Dependencies:" >}}
 * hostapd
 * iptables
 * iw
 * net-tools
 * python3
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
 [*] CaptiveFlask v1.0.2 - subtool from wifipumpkin3
 usage: captiveflask [-h] [-t TEMPLATE] [-s STATIC] [-r REDIRECT]
                     [-f FORCE_REDIRECT] [-v VERSION]
 
 CaptiveFlask - Server to create captive portal with flask doc:
 https://github.com/mh4x0f/captiveportals
 
 options:
   -h, --help            show this help message and exit
   -t TEMPLATE, --tamplate TEMPLATE
                         path the theme login captive portal
   -s STATIC, --static STATIC
                         path of the static files from webpage
   -r REDIRECT, --redirect REDIRECT
                         IpAddress from gataway captive portal
   -f FORCE_REDIRECT, --force-login_successful-template FORCE_REDIRECT
                         force redirect to login_successful.html template
   -v VERSION, --version VERSION
                         show version the tool
 ```
 
 - - -
 
 ##### sslstrip3
 
 
 ```
 root@kali:~# sslstrip3 -h
 
 sslstrip 0.9 by Moxie Marlinspike (mh4x0f)
 Fork: https://github.com/mh4x0f/sslstrip3
 Usage: sslstrip <options>
 
 Options:
 -w <filename>, --write=<filename> Specify file to log to (optional).
 -p , --post                       Log only SSL POSTs. (default)
 -s , --ssl                        Log all SSL traffic to and from server.
 -a , --all                        Log all SSL and HTTP traffic to and from server.
 -l <port>, --listen=<port>        Port to listen on (default 10000).
 -f , --favicon                    Substitute a lock favicon on secure requests.
 -k , --killsessions               Kill sessions in progress.
 -t <config>, --tamper <config>    Enable response tampering with settings from <config>.
 -i , --inject                     Inject code into HTML pages using a text file.
 -h                                print(this help message.
 
 ```
 
 - - -
 
 ##### wifipumpkin3
 
 
 ```
 root@kali:~# wifipumpkin3 --help
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
 
 ##### wp3
 
 
 ```
 root@kali:~# wp3 -h
 usage: wp3 [-h] [-i INTERFACE] [-s SESSION] [-p PULP] [-x XPULP]
            [-m WIRELESS_MODE] [--no-colors] [--rest] [--restport RESTPORT]
            [--username USERNAME] [--password PASSWORD] [-v]
 
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
