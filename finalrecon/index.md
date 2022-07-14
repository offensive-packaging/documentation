---
Title: finalrecon
Homepage: https://github.com/thewhiteh4t/FinalRecon
Repository: https://gitlab.com/kalilinux/packages/finalrecon
Architectures: all
Version: 1.1.3-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### finalrecon
 
  A fast and simple python script for web reconnaissance that follows
  a modular structure and provides detailed information on various areas.
 
 **Installed size:** `309 KB`  
 **How to install:** `sudo apt install finalrecon`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aiodns
 * python3-aiohttp
 * python3-bs4
 * python3-dnslib
 * python3-icmplib
 * python3-ipwhois
 * python3-lxml
 * python3-psycopg2
 * python3-requests
 * python3-tldextract
 {{< /spoiler >}}
 
 ##### finalrecon
 
 
 ```
 root@kali:~# finalrecon -h
 usage: finalrecon [-h] [--headers] [--sslinfo] [--whois] [--crawl] [--dns]
                   [--sub] [--trace] [--dir] [--ps] [--full] [-t T] [-T T]
                   [-w W] [-r] [-s] [-sp SP] [-d D] [-e E] [-m M] [-p P]
                   [-tt TT] [-o O]
                   url
 
 FinalRecon - The Last Web Recon Tool You Will Need | v1.1.3
 
 positional arguments:
   url         Target URL
 
 options:
   -h, --help  show this help message and exit
   --headers   Header Information
   --sslinfo   SSL Certificate Information
   --whois     Whois Lookup
   --crawl     Crawl Target
   --dns       DNS Enumeration
   --sub       Sub-Domain Enumeration
   --trace     Traceroute
   --dir       Directory Search
   --ps        Fast Port Scan
   --full      Full Recon
 
 Extra Options:
   -t T        Number of Threads [ Default : 30 ]
   -T T        Request Timeout [ Default : 30.0 ]
   -w W        Path to Wordlist [ Default : wordlists/dirb_common.txt ]
   -r          Allow Redirect [ Default : False ]
   -s          Toggle SSL Verification [ Default : True ]
   -sp SP      Specify SSL Port [ Default : 443 ]
   -d D        Custom DNS Servers [ Default : 1.1.1.1 ]
   -e E        File Extensions [ Example : txt, xml, php ]
   -m M        Traceroute Mode [ Default : UDP ] [ Available : TCP, ICMP ]
   -p P        Port for Traceroute [ Default : 80 / 33434 ]
   -tt TT      Traceroute Timeout [ Default : 1.0 ]
   -o O        Export Output [ Default : txt ] [ Available : xml, csv ]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
