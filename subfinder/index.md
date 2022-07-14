---
Title: subfinder
Homepage: https://github.com/projectdiscovery/subfinder
Repository: https://gitlab.com/kalilinux/packages/subfinder
Architectures: any
Version: 2.3.8-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### subfinder
 
  This package contains a subdomain discovery tool that discovers valid
  subdomains for websites by using passive online sources. It has a simple
  modular architecture and is optimized for speed. subfinder is built for doing
  one thing only - passive subdomain enumeration, and it does that very well.
 
 **Installed size:** `9.62 MB`  
 **How to install:** `sudo apt install subfinder`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### subfinder
 
 
 ```
 root@kali:~# subfinder -h
 Usage of subfinder:
   -cd
     	Upload results to the Chaos API (api-key required)
   -config string
     	Configuration file for API Keys, etc (default "/root/.config/subfinder/config.yaml")
   -d string
     	Domain to find subdomains for
   -dL string
     	File containing list of domains to enumerate
   -exclude-sources string
     	List of sources to exclude from enumeration
   -ls
     	List all available sources
   -max-time int
     	Minutes to wait for enumeration results (default 10)
   -nC
     	Don't Use colors in output
   -nW
     	Remove Wildcard & Dead Subdomains from output
   -o string
     	File to write output to (optional)
   -oD string
     	Directory to write enumeration results to (optional)
   -oI
     	Write output in Host,IP format
   -oJ
     	Write output in JSON lines Format
   -r string
     	Comma-separated list of resolvers to use
   -rL string
     	Text file containing list of resolvers to use
   -silent
     	Show only subdomains in output
   -sources string
     	Comma separated list of sources to use
   -t int
     	Number of concurrent goroutines for resolving (default 10)
   -timeout int
     	Seconds to wait before timing out (default 30)
   -v	Show Verbose output
   -version
     	Show version of subfinder
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
