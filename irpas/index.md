---
Title: irpas
Homepage: http://www.phenoelit.org/fr/tools.html
Repository: https://salsa.debian.org/pkg-security-team/irpas
Architectures: any
Version: 0.10-9
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### irpas
 
  This package contains a collection of programs used for advanced network
  operations, testing, and debugging.
   
  CDP and the route injectors can be useful in a production network.
  Several other tools are useful for security and firewall testing.
  Finally some tools such as netenum are useful for general admin
  scripting.
   
  Like all powerful tools, it could cause great damage, so be careful.
   
      * cdp - Cisco discovery protocol packet sender
      * igrp - IGRP route injector
      * ass - Autonomous system scanner
      * irdp - IRDP sender
      * irdpresponder - IRDP responder
      * itrace - ICMP based traceroute
      * tctrace - TCP SYN based traceroute
      * protos - ICMP based port scanner
      * netmask - Asks for netmask via ICMP
      * file2cable - Dumps any binary file direct to ethernet
      * dfkaa - Troubleshoot devices formerly known as Ascend (Pipeline, etc)
      * netenum - Ping scanner designed for shell scripts
      * hsrp - HSRP failover tester
      * icmp_redirect - ICMP redirection system
      * timestamp - ICMP timestamp requester
      * dhcpx - DHCP server "exerciser"
 
 **Installed size:** `406 KB`  
 **How to install:** `sudo apt install irpas`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### ass
 
 Autonomous system scanner
 
 ```
 root@kali:~# man ass
 ASS(1)                      General Commands Manual                     ASS(1)
 
 NAME
        ass - autonomous system scanner
 
 SYNOPSIS
        ass  [-v[v[v]]]   -i <interface> [-p] [-c] [-A] [-M] [-P IER12] -a <au-
        tonomous system start> -b <autonomous system stop> [-S <spoofed  source
        IP>] [-D <destination ip>] [-T <packets per delay>]
 
 DESCRIPTION
        This  manual  page documents briefly the ass command.  This manual page
        was written for the Debian distribution because  the  original  program
        does not have a manual page.
 
        ASS,  the  autonomous system scanner, is designed to find the AS of the
        router.  It supports the following protocols: IRDP, IGRP, EIGRP, RIPv1,
        RIPv2, CDP, HSRP and OSPF.
 
        In  passive  mode  (./ass -i eth0), it just listens to routing protocol
        packets (like broadcast and multicast hellos).
 
        In active mode (./ass -i eth0 -A), it tries to discover routers by ask-
        ing  for  information. This is done to the appropriate address for each
        protocol (either broadcast or multicast addresses). If  you  specify  a
        destination  address,  this will be used but may be not as effective as
        the defaults.
 
        EIGRP scanning is done differently: While  scanning,  ASS  listens  for
        HELLO  packets  and then scans the AS directly on the router who adver-
        tised himself. You can force EIGRP scanning into the same  AS-Scan  be-
        havior  as IGRP uses by giving a destination or into multicast scanning
        by the option -M.
 
        For Active mode, you can select the protocols you want to scan for.  If
        you  don't  select them, all are scanned. You select protcols by giving
        the option -P and any combination of the following chars: IER12, where:
 
        I = IGRP
 
        E = EIGRP
 
        R = IRDP
 
        1 = RIPv1
 
        2 = RIPv2
 
        ASS output might look a little strange, but has it's meanings:
 
        Routers are identified by the sender's IP address of the  packet.  This
        may lead to several routers showing up as more then one since they used
        different sender interfaces. In the brackets, the protocols this router
        runs are shown.
 
        Routing protocols are shown as one or more indented lines. First, there
        is the routing protocol name (like EIGRP), followed by  the  autonomous
        system  number  in brackets. Aligned to the right is the target network
        if applicable.
 
        IGRP routing info shows the target network and in brackets the  follow-
        ing values: Delay, Bandwidth, MTU, Reliability, Load and Hopcount.
 
        The  IRDP  info  is limmited to the announced gateway (router) and it's
        preference
 
        RIPv1 info just gives you the classified target network (remember RIPv1
        network boundaries) and it's metric
 
        RIPv2  info contains after the target network the following infos: Net-
        mask, next hop, arbitrary tag, and the metric. An additional  line  may
        appear  on the routers section that gives you the authentication if en-
        abled in the protocol. For text auth, the password is there.
 
        The basic EIGRP just gives you the autonomous system  number,  the  IOS
        and EIGRP version as found in the HELLO packet
 
        The  EIGRP routes section depends on the type of route. All of them in-
        clude the fields destination network, destination mask and in the  last
        line  (in  brackets) the values for Delay, Bandwidth, MTU, Reliability,
        Load and Hopcount. External routes also include the originating router,
        the  originating  autonomous system, the external metric and the source
        of this route.
 
        HSRP info is not routing, therefore the third field is the  virtual  IP
        address  of  the standby group, followed by the state, the auth string,
        Hello, Hold and priority values.
 
        OSPF info includes the destination network as well as the  Area  in  IP
        format,  the  authentication used (and, if applicable the auth string),
        netmask, designated and backup router and the values for Dead, Priority
        and Hello.
 
 OPTIONS
        A summary of options is included below.
 
        -h     Show summary of options.
 
        -i <interface>
               interface
 
        -v     verbose mode
 
        -A     Active mode scanning
 
        -P <protocols>
               Select protocols to scan
 
        -M     EIGRP systems are scanned using the multicast address and not by
               HELLO enumeration and direct query
 
        -a <autonomous system>
               autonomous system to start from
 
        -b <autonomous system>
               autonomous system to stop with
 
        -S <spoofed source IP>
               maybe you need this
 
        -D <destination IP>
               If you don't specify this, the appropriate address per  protocol
               is used
 
        -p     don't run in promiscuous mode (bad idea)
 
        -c     terminate  after scanning. This is not recommended since answers
               may arrive later and you could see some  traffic  that  did  not
               show up during your scans
 
        -T <packets per delay>
               how  many  packets should we wait some milliseconds (-T 1 is the
               slowest scan -T 100 begins to become unreliable)
 
 AUTHOR
        This manual page was written by Vince Mulhollon  <vlm@debian.org>,  for
        the Debian GNU/Linux system (but may be used by others).
 
                                December 16, 2002                        ASS(1)
 ```
 
 - - -
 
 ##### cdp
 
 Cdp packet generator
 
 ```
 root@kali:~# cdp -h
 cdp [-v] -i <interface> -m {0,1} ...
 
 Flood mode (-m 0):
 -n <number>	number of packets
 -l <number>	length of the device id
 -c <char>	character to fill in device id
 -r		randomize device id string
 
 Spoof mode (-m 1):
 -D <string>	Device id
 -P <string>	Port id
 -L <string>	Platform
 -S <string>	Software
 -F <string>	IP address
 -C <capabilities>
 	these are:
 	R - Router, T - Trans Bridge, B - Source Route Bridge
 	S - Switch, H - Host, I - IGMP, r - Repeater
 ```
 
 - - -
 
 ##### dfkaa
 
 
 ```
 root@kali:~# dfkaa -h
 dfkaa: invalid option -- 'h'
 Usage ... well. Look into the .c
 ```
 
 - - -
 
 ##### dhcpx
 
 
 ```
 root@kali:~# dhcpx -h
 dhcpx [-v[v[v]]] -i <interface> [-A] 
 	[-D <destination ip>]
 	[-t <discovery time in secs>]
 	[-u <ARP time in secs>]
 ```
 
 - - -
 
 ##### file2cable
 
 Sends a file as a raw ethernet frame
 
 ```
 root@kali:~# file2cable -h
 file2cable [-v] -i <interface> -f <file>
 ```
 
 - - -
 
 ##### hsrp
 
 
 ```
 root@kali:~# hsrp -h
 hsrp -i <interface> -v <virtual IP> -d <router ip> -a <authword>
 	-g <group> [-S <source>]
 EXAMPLE:
 while (true);
   do (./hsrp -d 224.0.0.2 -v192.168.1.22 -a cisco -g 1 -i eth0 ; sleep 3);
 done
 ```
 
 - - -
 
 ##### icmp_redirect
 
 
 ```
 root@kali:~# icmp_redirect -h
 icmp_redirect [-v[v[v]]] -i <interface> 
 	[-s <source net>/<source mask>]
 	[-d <destination net>/<destination mask>]
 	[-G <gateway IP>] [-w <delay>]
 	[-S <ip address>]
 ```
 
 - - -
 
 ##### igrp
 
 Igrp route injector
 
 ```
 root@kali:~# igrp -h
 Usage: 
 igrp [-v[v[v]]] -i <interface> -f <routes file> 
 	-a <autonomous system> [-b brute force end]
 	[-S <spoofed source IP>] [-D <destination ip>]
 ```
 
 - - -
 
 ##### inetmask
 
 Ask for the netmask via ICMP
 
 ```
 root@kali:~# inetmask -h
 inetmask: invalid option -- 'h'
 Usage: inetmask -d <destination> -t <timeout>
 ```
 
 - - -
 
 ##### irdp
 
 Irdp packet sender
 
 ```
 root@kali:~# irdp -h
 Usage: 
 irdp [-v (useless)] -i <interface> 
 	[-S <spoofed source IP>] [-D <destination ip>]
 	[-l <lifetime in sec, default: 1800>] [-p <preference>]
 ```
 
 - - -
 
 ##### irdpresponder
 
 Irdpresponder packet sender
 
 ```
 root@kali:~# irdpresponder -h
 Usage: 
 irdpresponder [-v[v[v]]] -i <interface>
 	[-S <spoofed source IP>] [-D <destination ip>]
 	[-l <lifetime in sec, default: 1800>] [-p <preference>]
 ```
 
 - - -
 
 ##### itrace
 
 Similar to traceroute, yet uses ICMP echo
 
 ```
 root@kali:~# itrace -h
 itrace: invalid option -- 'h'
 Usage: itrace [-vn] [-pX] [-mX] [-tX] -i<dev> -d<destination>
 
 -v	verbose
 -n	reverse lookup IPs
 -pX	send X probes (default=3)
 -mX	maximum TTL (default=30)
 -tX	timeout X sec (default=3)
 -i<dev>	use this device
 -d<des>	trace to this destination
 ```
 
 - - -
 
 ##### netenum
 
 
 ```
 root@kali:~# netenum -h
 error in enumerate
 ```
 
 - - -
 
 ##### protos
 
 
 ```
 root@kali:~# protos -h
 Usage: ./protos -i eth0 -d 10.1.2.3 -v
 -v             verbose
 -V             show which protocols are not supported
 -u             don't ping targets first
 -s             make the scan slow (for very remote devices)
 -L             show the long protocol name and it's reference (RFC)
 -p x           number of probes (default=5)
 -S x           sleeptime is x (default=1)
 -a x           continue scan afterwards for x seconds (default=3)
 -d dest        destination (IP or IP/MASK)
 -i interface   the eth0 stuff
 -W             don't scan, just print the protocol list
 ```
 
 - - -
 
 ##### tctrace
 
 Similar to traceroute, yet uses TCP SYN packets
 
 ```
 root@kali:~# tctrace -h
 tctrace: invalid option -- 'h'
 Usage: tctrace [-vn] [-pX] [-mX] [-tX] [-DX] [-SX] -i<dev> -d<destination>
 
 -v	verbose
 -n	reverse lookup IPs
 -pX	send X probes (default=3)
 -mX	maximum TTL (default=30)
 -tX	timeout X sec (default=3)
 -DX	destination port (default=80)
 -SX	source port (default=1064)
 -i<dev>	use this device
 -d<des>	trace to this destination
 ```
 
 - - -
 
 ##### timestamp
 
 
 ```
 root@kali:~# timestamp -h
 timestamp: invalid option -- 'h'
 Usage: timestamp -d <destination> -t <timeout>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
