---
Title: spectools
Homepage: http://www.kismetwireless.net/spectools/
Repository: https://anonscm.debian.org/gitweb/?p=collab-maint/spectools.git
Architectures: any
Version: 201601r1-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### spectools
 
  Spectrum-Tools is a set of utilities for using the Wi-Spy USB spectrum
  analyzer tools from Metageek LLC.  They include userspace drivers for
  the hardware (implemented via libusb), a graphing UI built on GTK/Cairo,
  network servers for remote devices, and simple utilities for developing
  additional tools.
 
 **Installed size:** `364 KB`  
 **How to install:** `sudo apt install spectools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcairo2 
 * libgdk-pixbuf-2.0-0 
 * libglib2.0-0 
 * libgtk2.0-0 
 * libncurses6 
 * libpango-1.0-0 
 * libtinfo6 
 * libusb-0.1-4 
 {{< /spoiler >}}
 
 ##### spectool_curses
 
 Utility for developing other tools using the Wi-Spy
 
 ```
 root@kali:~# spectool_curses -h
 spectool_curses [ options ]
  -n / --net  tcp://host:port  Connect to network server
  -l / --list                  List detected devices
  -r / --range #               Use device range #
  -d / --device #              Use device #
 ```
 
 - - -
 
 ##### spectool_gtk
 
 2.4 GHz spectrum analysis using the Wi-Spy
 
 ```
 root@kali:~# man spectool_gtk
 SPECTOOLS(1)                General Commands Manual               SPECTOOLS(1)
 
 NAME
        spectool_gtk -- 2.4 GHz spectrum analysis using the Wi-Spy
 
 SYNOPSIS
        spectool_gtk
 
 DESCRIPTION
        spectool_gtk is a graphing UI for spectrum analysis on the 2.4 GHz band
        using the Wi-Spy hardware device.
 
 SEE ALSO
        spectool_curses (1), spectool_net (1), spectool_raw (1).
 
 AUTHOR
        This manual page was written by Francois  Marier  <francois@debian.org>
        for  the  Debian  system  (but  may  be used by others).  Permission is
        granted to copy, distribute and/or modify this document under the terms
        of  the  GNU  General  Public License, Version 3 any later version pub-
        lished by the Free Software Foundation.
 
        On Debian systems, the complete text of the GNU General Public  License
        can be found in /usr/share/common-licenses/GPL.
 
                                                                   SPECTOOLS(1)
 ```
 
 - - -
 
 ##### spectool_net
 
 Network server for the spectool_gtk program
 
 ```
 root@kali:~# man spectool_net
 SPECTOOLS(1)                General Commands Manual               SPECTOOLS(1)
 
 NAME
        spectool_net -- Network server for the spectool_gtk program
 
 SYNOPSIS
        spectool_net [-b secs]  [-p port]  [-a bind address]
 
 DESCRIPTION
        spectool_net is network server to which spectool_gtk can connect.
 
 OPTIONS
        This  program  follows the usual GNU command line syntax, with long op-
        tions starting with two dashes (`-').  A summary of options is included
        below.
 
        -h           --help
                  Show summary of options.
 
        -b secs           --broadcast secs
                  Send broadcast announce.
 
        -p port           --port port
                  Use alternate port.
 
        -a address           --bindaddr address
                  Bind to specific address.
 
 SEE ALSO
        spectool_gtk (1), spectool_curses (1), spectool_raw (1).
 
 AUTHOR
        This  manual  page was written by Francois Marier <francois@debian.org>
        for the Debian system (but may  be  used  by  others).   Permission  is
        granted to copy, distribute and/or modify this document under the terms
        of the GNU General Public License, Version 3  any  later  version  pub-
        lished by the Free Software Foundation.
 
        On  Debian systems, the complete text of the GNU General Public License
        can be found in /usr/share/common-licenses/GPL.
 
                                                                   SPECTOOLS(1)
 ```
 
 - - -
 
 ##### spectool_raw
 
 Utility for developing other tools using the Wi-Spy
 
 ```
 root@kali:~# spectool_raw -h
 spectool_raw [ options ]
  -n / --net  tcp://host:port  Connect to network server instead of
  -b / --broadcast             Listen for (and connect to) broadcast servers
  -l / --list				  List devices and ranges only
  -r / --range [device:]range  Configure a device for a specific range
                               local USB devices
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
