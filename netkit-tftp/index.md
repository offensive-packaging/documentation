---
Title: netkit-tftp
Homepage: 
Repository: 
Architectures: all
Version: 0.17-25
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tftp
 
  This is a transitional package. It can safely be removed.
 
 **Installed size:** `14 KB`  
 **How to install:** `sudo apt install tftp`  
 
 {{< spoiler "Dependencies:" >}}
 * tftp-hpa
 {{< /spoiler >}}
 
 ##### tftp
 
 IPv4 Trivial File Transfer Protocol client
 
 ```
 root@kali:~# tftp -h
 Usage: tftp [-4][-6][-v][-l][-m mode] [host [port]] [-c command]
 ```
 
 - - -
 
 ##### tftp
 
 IPv4 Trivial File Transfer Protocol client
 
 ```
 root@kali:~# tftp -h
 Usage: tftp [-4][-6][-v][-l][-m mode] [host [port]] [-c command]
 ```
 
 - - -
 
 ### tftpd
 
  Tftpd is a server which supports the Internet Trivial File Transfer Protocol
  (RFC 783).  The TFTP server operates at the port indicated in the `tftp'
  service description; see services(5).  The server is normally started by
  inetd(8).
   
  Warning: Does not support 'tsize', which is required by some tftp clients,
  especially PXE, and various other network boot clients. For those, use atftpd
  or tftpd-hpa.
 
 **Installed size:** `50 KB`  
 **How to install:** `sudo apt install tftpd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * openbsd-inetd | inet-superserver
 {{< /spoiler >}}
 
 ##### in.tftpd
 
 DARPA Trivial File Transfer Protocol server
 
 ```
 root@kali:~# man in.tftpd
 TFTPD(8)                  BSD System Manager's Manual                 TFTPD(8)
 
 NAME
      tftpd -- DARPA Trivial File Transfer Protocol server
 
 SYNOPSIS
      tftpd [-n] [-s] [directory ...]
 
 DESCRIPTION
      Tftpd is a server which supports the DARPA Trivial File Transfer Proto-
      col.  The TFTP server operates at the port indicated in the 'tftp' ser-
      vice description; see services(5).  The server is normally started by
      inetd(8).
 
      The use of tftp(1) does not require an account or password on the remote
      system.  Due to the lack of authentication information, tftpd will allow
      only publicly readable files to be accessed.  Files may be written only
      if they already exist and are publicly writable.  Note that this extends
      the concept of "public" to include all users on all hosts that can be
      reached through the network; this may not be appropriate on all systems,
      and its implications should be considered before enabling tftp service.
      The server should have the user ID with the lowest possible privilege.
 
      Access to files may be controlled by invoking tftpd with a list of direc-
      tories by including pathnames as server program arguments in
      /etc/inetd.conf.  In this case access is restricted to files whose names
      are prefixed by the one of the given directories. If no directories are
      supplied the default is /tftpboot.  To give out access to the whole
      filesystem, should this be desired for some reason, supply / as an argu-
      ment.
 
      Unfortunately, on multi-homed systems, it is impossible for tftpd to de-
      termine the address on which a packet was received. As a result, tftpd
      uses two different mechanisms to guess the best source address to use for
      replies. If the socket that inetd(8) passed to tftpd is bound to a par-
      ticular address, tftpd uses that address for replies. Otherwise, tftpd
      uses ``UDP connect'' to let the kernel choose the reply address based on
      the destination of the replies and the routing tables. This means that
      most setups will work transparently, while in cases where the reply ad-
      dress must be fixed, the virtual hosting feature of inetd(8) can be used
      to ensure that replies go out from the correct address.  These considera-
      tions are important, because most tftp clients will reject reply packets
      that appear to come from an unexpected address.
 
      The options are:
 
      -n      Suppresses negative acknowledgement of requests for nonexistent
              relative filenames.
 
      -s      All absolute filenames are treated as if they were preceded by
              the first directory argument, or /tftpboot if there is none.
 
 SEE ALSO
      tftp(1), inetd(8)
 
 HISTORY
      The tftpd command appeared in 4.2BSD.
 
 Linux NetKit (0.17)              July 29, 2000             Linux NetKit (0.17)
 ```
 
 - - -
 
 ##### in.tftpd
 
 DARPA Trivial File Transfer Protocol server
 
 ```
 root@kali:~# man in.tftpd
 TFTPD(8)                  BSD System Manager's Manual                 TFTPD(8)
 
 NAME
      tftpd -- DARPA Trivial File Transfer Protocol server
 
 SYNOPSIS
      tftpd [-n] [-s] [directory ...]
 
 DESCRIPTION
      Tftpd is a server which supports the DARPA Trivial File Transfer Proto-
      col.  The TFTP server operates at the port indicated in the 'tftp' ser-
      vice description; see services(5).  The server is normally started by
      inetd(8).
 
      The use of tftp(1) does not require an account or password on the remote
      system.  Due to the lack of authentication information, tftpd will allow
      only publicly readable files to be accessed.  Files may be written only
      if they already exist and are publicly writable.  Note that this extends
      the concept of "public" to include all users on all hosts that can be
      reached through the network; this may not be appropriate on all systems,
      and its implications should be considered before enabling tftp service.
      The server should have the user ID with the lowest possible privilege.
 
      Access to files may be controlled by invoking tftpd with a list of direc-
      tories by including pathnames as server program arguments in
      /etc/inetd.conf.  In this case access is restricted to files whose names
      are prefixed by the one of the given directories. If no directories are
      supplied the default is /tftpboot.  To give out access to the whole
      filesystem, should this be desired for some reason, supply / as an argu-
      ment.
 
      Unfortunately, on multi-homed systems, it is impossible for tftpd to de-
      termine the address on which a packet was received. As a result, tftpd
      uses two different mechanisms to guess the best source address to use for
      replies. If the socket that inetd(8) passed to tftpd is bound to a par-
      ticular address, tftpd uses that address for replies. Otherwise, tftpd
      uses ``UDP connect'' to let the kernel choose the reply address based on
      the destination of the replies and the routing tables. This means that
      most setups will work transparently, while in cases where the reply ad-
      dress must be fixed, the virtual hosting feature of inetd(8) can be used
      to ensure that replies go out from the correct address.  These considera-
      tions are important, because most tftp clients will reject reply packets
      that appear to come from an unexpected address.
 
      The options are:
 
      -n      Suppresses negative acknowledgement of requests for nonexistent
              relative filenames.
 
      -s      All absolute filenames are treated as if they were preceded by
              the first directory argument, or /tftpboot if there is none.
 
 SEE ALSO
      tftp(1), inetd(8)
 
 HISTORY
      The tftpd command appeared in 4.2BSD.
 
 Linux NetKit (0.17)              July 29, 2000             Linux NetKit (0.17)
 ```
 
 - - -
 
 ##### in.tftpd
 
 DARPA Trivial File Transfer Protocol server
 
 ```
 root@kali:~# man in.tftpd
 TFTPD(8)                  BSD System Manager's Manual                 TFTPD(8)
 
 NAME
      tftpd -- DARPA Trivial File Transfer Protocol server
 
 SYNOPSIS
      tftpd [-n] [-s] [directory ...]
 
 DESCRIPTION
      Tftpd is a server which supports the DARPA Trivial File Transfer Proto-
      col.  The TFTP server operates at the port indicated in the 'tftp' ser-
      vice description; see services(5).  The server is normally started by
      inetd(8).
 
      The use of tftp(1) does not require an account or password on the remote
      system.  Due to the lack of authentication information, tftpd will allow
      only publicly readable files to be accessed.  Files may be written only
      if they already exist and are publicly writable.  Note that this extends
      the concept of "public" to include all users on all hosts that can be
      reached through the network; this may not be appropriate on all systems,
      and its implications should be considered before enabling tftp service.
      The server should have the user ID with the lowest possible privilege.
 
      Access to files may be controlled by invoking tftpd with a list of direc-
      tories by including pathnames as server program arguments in
      /etc/inetd.conf.  In this case access is restricted to files whose names
      are prefixed by the one of the given directories. If no directories are
      supplied the default is /tftpboot.  To give out access to the whole
      filesystem, should this be desired for some reason, supply / as an argu-
      ment.
 
      Unfortunately, on multi-homed systems, it is impossible for tftpd to de-
      termine the address on which a packet was received. As a result, tftpd
      uses two different mechanisms to guess the best source address to use for
      replies. If the socket that inetd(8) passed to tftpd is bound to a par-
      ticular address, tftpd uses that address for replies. Otherwise, tftpd
      uses ``UDP connect'' to let the kernel choose the reply address based on
      the destination of the replies and the routing tables. This means that
      most setups will work transparently, while in cases where the reply ad-
      dress must be fixed, the virtual hosting feature of inetd(8) can be used
      to ensure that replies go out from the correct address.  These considera-
      tions are important, because most tftp clients will reject reply packets
      that appear to come from an unexpected address.
 
      The options are:
 
      -n      Suppresses negative acknowledgement of requests for nonexistent
              relative filenames.
 
      -s      All absolute filenames are treated as if they were preceded by
              the first directory argument, or /tftpboot if there is none.
 
 SEE ALSO
      tftp(1), inetd(8)
 
 HISTORY
      The tftpd command appeared in 4.2BSD.
 
 Linux NetKit (0.17)              July 29, 2000             Linux NetKit (0.17)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
