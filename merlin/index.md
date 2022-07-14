---
Title: merlin
Homepage: https://github.com/Ne0nd0g/merlin
Repository: https://gitlab.com/kalilinux/packages/merlin
Architectures: any
Version: 0.10.0~beta+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### merlin-agent
 
  This package contains a cross-platform post-exploitation HTTP/2 Command &
  Control server and agent written in golang.
 
 **Installed size:** `8.46 MB`  
 **How to install:** `sudo apt install merlin-agent`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### merlinagent
 
 
 ```
 root@kali:~# merlinagent -h
 Merlin Agent
 ```
 
 - - -
 
 ### merlin-server
 
  This package contains a cross-platform post-exploitation HTTP/2 Command &
  Control server and agent written in golang.
 
 **Installed size:** `24.43 MB`  
 **How to install:** `sudo apt install merlin-server`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjs-sphinxdoc 
 * sphinx-rtd-theme-common 
 {{< /spoiler >}}
 
 ##### merlinserver
 
 
 ```
 root@kali:~# merlinserver -h
 #################################################
 #		MERLIN SERVER			#
 #################################################
 Version: 0.10.0-beta
 Build: nonRelease
 Merlin Server does not take any command line arguments
 Visit the Merlin wiki for additional information: https://merlin-c2.readthedocs.io/en/latest/
 ```
 
 - - -
 
 ### prism
 
  This package contains a Merlin server identification tool.
 
 **Installed size:** `8.60 MB`  
 **How to install:** `sudo apt install prism`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### prism
 
 
 ```
 root@kali:~# prism -h
 Merlin PRISM
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
