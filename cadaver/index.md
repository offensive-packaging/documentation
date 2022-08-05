---
Title: cadaver
Homepage: http://www.webdav.org/cadaver/
Repository: http://git.tokkee.org/?p=pkg-cadaver.git
Architectures: any
Version: 0.23.3-2.2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-web 
Icon: images/cadaver-logo.svg
PackagesInfo: |
 ### cadaver
 
  cadaver supports file upload, download, on-screen display, in-place editing,
  namespace operations (move/copy), collection creation and deletion, property
  manipulation, and resource locking.
   
  Its operation is similar to the standard BSD ftp(1) client and the Samba
  Project's smbclient(1).
   
  This package includes GnuTLS (HTTPS) support.
   
  WebDAV (Web-based Distributed Authoring and Versioning) is a set of
  extensions to the HTTP protocol which allow users to collaboratively edit and
  manage files on remote web servers.
 
 **Installed size:** `242 KB`  
 **How to install:** `sudo apt install cadaver`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libneon27-gnutls
 * libreadline8 
 {{< /spoiler >}}
 
 ##### cadaver
 
 A command-line WebDAV client for Unix.
 
 ```
 root@kali:~# cadaver -h
 Usage: cadaver [OPTIONS] http://hostname[:port]/path
   Port defaults to 80, path defaults to '/'
 Options:
   -t, --tolerant            Allow cd/open into non-WebDAV enabled collection.
   -r, --rcfile=FILE         Read script from FILE instead of ~/.cadaverrc.
   -p, --proxy=PROXY[:PORT]  Use proxy host PROXY and optional proxy port PORT.
   -V, --version             Display version information.
   -h, --help                Display this help message.
 Please send bug reports and feature requests to <cadaver@webdav.org>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
