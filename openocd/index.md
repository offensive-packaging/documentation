---
Title: openocd
Homepage: http://openocd.sourceforge.net/
Repository: https://salsa.debian.org/electronics-team/openocd
Architectures: any
Version: 0.11.0-1
Metapackages: kali-linux-everything kali-tools-hardware 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### openocd
 
  OpenOCD aims to provide debugging, in-system programming and boundary-scan
  testing for embedded target devices.
   
  The debugger uses an IEEE 1149-1 compliant JTAG TAP bus master to access
  on-chip debug functionality available on ARM based microcontrollers or
  system-on-chip solutions. For MIPS systems the EJTAG interface is supported.
  Additionally there is support for eSi-RISC, Intel, OpenRISC, RISC-V and ARC
  controllers.
   
  User interaction is realized through a telnet command line interface,
  a gdb (the GNU debugger) remote protocol server, and a simplified RPC
  connection that can be used to interface with OpenOCD's Jim Tcl engine.
   
  OpenOCD supports many different types of JTAG interfaces/programmers.
 
 **Installed size:** `8.00 MB`  
 **How to install:** `sudo apt install openocd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcapstone4 
 * libftdi1-2 
 * libgpiod2 
 * libhidapi-hidraw0 
 * libjaylink0 
 * libjim0.81 
 * libusb-0.1-4 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 ##### openocd
 
 A free and open on-chip debugging, in-system programming and boundary-scan testing tool for ARM and MIPS systems
 
 ```
 root@kali:~# man openocd
 OPENOCD(1)                  General Commands Manual                 OPENOCD(1)
 
 NAME
        openocd  - A free and open on-chip debugging, in-system programming and
        boundary-scan testing tool for ARM and MIPS systems
 
 SYNOPSIS
        openocd [-fsdlcphv] [--file <filename>] [--search  <dirname>]  [--debug
        <debuglevel>]  [--log_output  <filename>]  [--command  <cmd>]  [--pipe]
        [--help] [--version]
 
 DESCRIPTION
        OpenOCD is an  on-chip  debugging,  in-system  programming  and  bound-
        ary-scan testing tool for various ARM and MIPS systems.
 
        The  debugger  uses an IEEE 1149-1 compliant JTAG TAP bus master to ac-
        cess on-chip debug  functionality  available  on  ARM  based  microcon-
        trollers or system-on-chip solutions. For MIPS systems the EJTAG inter-
        face is supported.
 
        User interaction is realized through a telnet command line interface, a
        gdb  (the  GNU  debugger)  remote protocol server, and a simplified RPC
        connection that can be used to interface with OpenOCD's Jim Tcl engine.
 
        OpenOCD supports various different types  of  JTAG  interfaces/program-
        mers, please check the openocd info page for the complete list.
 
 OPTIONS
        -f, --file <filename>
               This is a shortcut for a -c "[script <filename>]" command, using
               a search path to load the configuration file <filename>.  In or-
               der  to  specify  multiple  config  files,  you can use multiple
               --file arguments. If no such -c options are included, the  first
               config file openocd.cfg in the search path will be used.
 
        -s, --search <dirname>
               Add  <dirname>  to  the  search  path  used for config files and
               scripts.  The search path begins  with  the  current  directory,
               then  includes  these additional directories before other compo-
               nents such as the standard OpenOCD script libraries.
 
        -d, --debug <debuglevel>
               Set debug level. Possible values are:
                 * 0 (errors)
                 * 1 (warnings)
                 * 2 (informational messages)
                 * 3 (debug messages)
               The default level is 2.
 
        -l, --log_output <filename>
               Redirect log output to the file <filename>.  Per default the log
               output is printed on stderr.
 
        -c, --command <cmd>
               Add  the  command <cmd> to a list of commands executed on server
               startup.  Note that you will need to explicitly invoke  init  if
               the command requires access to a target or flash.
 
        -p, --pipe
               Use pipes when talking to gdb.
 
        -h, --help
               Show a help text and exit.
 
        -v, --version
               Show version information and exit.
 
 BUGS
        Please   report   any   bugs   on   the  mailing  list  at  openocd-de-
        vel@lists.sourceforge.net.
 
 LICENCE
        OpenOCD is covered by the GNU General Public License (GPL),  version  2
        or later.
 
 SEE ALSO
        jtag(1)
 
        The  full  documentation for openocd is maintained as a Texinfo manual.
        If the info (or pinfo) and openocd programs are properly  installed  at
        your  site, the command info openocd should give you access to the com-
        plete manual.
 
 AUTHORS
        Please see the file AUTHORS.
 
        This manual page was written by Uwe Hermann  <uwe@hermann-uwe.de>.   It
        is licensed under the terms of the GNU GPL (version 2 or later).
 
                                November 24, 2009                    OPENOCD(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
