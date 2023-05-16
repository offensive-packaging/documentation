---
Title: sslh
Homepage: http://www.rutschle.net/tech/sslh/README.html
Repository: https://salsa.debian.org/debian/sslh.git
Architectures: any
Version: 1.20-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-post-exploitation kali-tools-web 
Icon: images/sslh-logo.svg
PackagesInfo: |
 ### sslh
 
  sslh lets one accept HTTPS, SSH, OpenVPN, tinc and XMPP connections on the
  same port. This makes it possible to connect to any of these servers on
  port 443 (e.g. from inside a corporate firewall, which almost never block
  port 443) while still serving HTTPS on that port.
 
 **Installed size:** `178 KB`  
 **How to install:** `sudo apt install sslh`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * debconf 
 * init-system-helpers 
 * libc6 
 * libcap2 
 * libconfig9
 * libpcre3
 * libwrap0 
 * lsb-base 
 * update-inetd
 {{< /spoiler >}}
 
 ##### sslh
 
 Protocol demultiplexer
 
 ```
 root@kali:~# sslh -h
 sslh: option '-http' requires an argument
 sslh 1.20-1+b2
 usage:
 	sslh  [-v] [-i] [-V] [-f] [-n] [--transparent] [-F<file>]
 	[-t <timeout>] [-P <pidfile>] [-u <username>] [-C <chroot>] -p <addr> [-p <addr> ...] 
 	[--ssh <addr>]
 	[--openvpn <addr>]
 	[--tinc <addr>]
 	[--xmpp <addr>]
 	[--http <addr>]
 	[--tls <addr>]
 	[--adb <addr>]
 	[--socks5 <addr>]
 	[--anyprot <addr>]
 
 
 	[--on-timeout <addr>]
 -v: verbose
 -V: version
 -f: foreground
 -n: numeric output
 -u: specify under which user to run
 -C: specify under which chroot path to run
 --transparent: behave as a transparent proxy
 -F: use configuration file (warning: no space between -F and file name!)
 --on-timeout: connect to specified address upon timeout (default: ssh address)
 -t: seconds to wait before connecting to --on-timeout address.
 -p: address and port to listen on.
     Can be used several times to bind to several addresses.
 --[ssh,ssl,...]: where to connect connections from corresponding protocol.
 -P: PID file.
 -i: Run as a inetd service.
 ```
 
 - - -
 
 ##### sslh-select
 
 Protocol demultiplexer
 
 ```
 root@kali:~# sslh-select -h
 sslh-select: option '-http' requires an argument
 sslh 1.20-1+b2
 usage:
 	sslh  [-v] [-i] [-V] [-f] [-n] [--transparent] [-F<file>]
 	[-t <timeout>] [-P <pidfile>] [-u <username>] [-C <chroot>] -p <addr> [-p <addr> ...] 
 	[--ssh <addr>]
 	[--openvpn <addr>]
 	[--tinc <addr>]
 	[--xmpp <addr>]
 	[--http <addr>]
 	[--tls <addr>]
 	[--adb <addr>]
 	[--socks5 <addr>]
 	[--anyprot <addr>]
 
 
 	[--on-timeout <addr>]
 -v: verbose
 -V: version
 -f: foreground
 -n: numeric output
 -u: specify under which user to run
 -C: specify under which chroot path to run
 --transparent: behave as a transparent proxy
 -F: use configuration file (warning: no space between -F and file name!)
 --on-timeout: connect to specified address upon timeout (default: ssh address)
 -t: seconds to wait before connecting to --on-timeout address.
 -p: address and port to listen on.
     Can be used several times to bind to several addresses.
 --[ssh,ssl,...]: where to connect connections from corresponding protocol.
 -P: PID file.
 -i: Run as a inetd service.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
