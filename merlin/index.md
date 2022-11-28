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
   -debug
     	Enable debug output
   -host string
     	HTTP Host header
   -ja3 string
     	JA3 signature string (not the MD5 hash). Overrides -proto flag
   -killdate string
     	The date, as a Unix EPOCH timestamp, that the agent will quit running (default "0")
   -maxretry string
     	The maximum amount of failed checkins before the agent will quit running (default "7")
   -padding string
     	The maximum amount of data that will be randomly selected and appended to every message (default "4096")
   -proto string
     	Protocol for the agent to connect with [https (HTTP/1.1), http (HTTP/1.1 Clear-Text), h2 (HTTP/2), h2c (HTTP/2 Clear-Text), http3 (QUIC or HTTP/3.0)] (default "h2")
   -proxy string
     	Hardcoded proxy to use for http/1.1 traffic only that will override host configuration
   -psk string
     	Pre-Shared Key used to encrypt initial communications (default "merlin")
   -skew string
     	Amount of skew, or variance, between agent checkins (default "3000")
   -sleep string
     	Time for agent to sleep (default "30s")
   -url string
     	Full URL for agent to connect to (default "https://127.0.0.1:443")
   -useragent string
     	The HTTP User-Agent header string that the Agent will use while sending traffic (default "Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/40.0.2214.85 Safari/537.36")
   -v	Enable verbose output
   -version
     	Print the agent version and exit
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
   -debug
     	Enable debug output
   -host string
     	HTTP Host header
   -ja3 string
     	JA3 signature string (not the MD5 hash). Overrides -proto flag
   -proto string
     	Protocol for the agent to connect with [https (HTTP/1.1), h2 (HTTP/2), hq (QUIC or HTTP/3.0)] (default "h2")
   -proxy string
     	Hardcoded proxy to use for http/1.1 traffic only that will override host configuration
   -psk string
     	Pre-Shared Key used to encrypt initial communications (default "merlin")
   -url string
     	Full URL for agent to connect to (default "https://127.0.0.1:443")
   -verbose
     	Enable verbose output
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
