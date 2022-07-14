---
Title: sliver
Homepage: https://github.com/BishopFox/sliver
Repository: https://gitlab.com/kalilinux/packages/sliver
Architectures: any
Version: 1.1.1-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sliver
 
  This package contains a general purpose cross-platform implant framework that
  supports C2 over Mutual-TLS, HTTP(S), and DNS. Implants are dynamically
  compiled with unique X.509 certificates signed by a per-instance certificate
  authority generated when you first run the binary.
 
 **Installed size:** `181.23 MB`  
 **How to install:** `sudo apt install sliver`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sliver-server
 
 
 ```
 root@kali:~# sliver-server -h
 Usage:
   sliver-server [flags]
   sliver-server [command]
 
 Available Commands:
   export-ca   Export certificate authority
   help        Help about any command
   import-ca   Import certificate authority
   operator    Generate operator configuration files
   unpack      Unpack assets and exit
   version     Print version and exit
 
 Flags:
   -h, --help   help for sliver-server
 
 Use "sliver-server [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
