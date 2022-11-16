---
Title: dnstwist
Homepage: https://github.com/elceef/dnstwist
Repository: https://salsa.debian.org/pkg-security-team/dnstwist
Architectures: all
Version: 0~20221022-1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dnstwist
 
  dnstwist generates a list of similarly looking domain names for
  a given domain name and performs DNS queries for them (A, AAAA,
  NS and MX). For MX records it checks whether there is an active mail
  server which could be used to intercept misdirected emails.
  Additionally it estimates webpage similarity based on fuzzy hashes.
  This functionality might be helpful in detecting typosquatters, phishing
  attacks, fraud and corporate espionage.
 
 **Installed size:** `660 KB`  
 **How to install:** `sudo apt install dnstwist`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### dnstwist
 
 Domain name permutation engine
 
 ```
 root@kali:~# dnstwist -h
 dnstwist 20221022 by <marcin@ulikowski.pl>
 
 usage: /usr/bin/dnstwist [OPTION]... DOMAIN
 
 Domain name permutation engine for detecting homograph phishing attacks,
 typosquatting, fraud and brand impersonation.
 
 positional arguments:
   domain                      Domain name or URL to scan
 
 options:
   -a, --all                   Show all DNS records
   -b, --banners               Determine HTTP and SMTP service banners
   -d FILE, --dictionary FILE  Generate more domains using dictionary FILE
   -f FORMAT, --format FORMAT  Output format: cli, csv, json, list (default:
                               cli)
   --fuzzers LIST              Use only selected fuzzing algorithms (separated
                               with commas)
   -g, --geoip                 Lookup for GeoIP location
   -m, --mxcheck               Check if MX can be used to intercept emails
   -o FILE, --output FILE      Save output to FILE
   -r, --registered            Show only registered domain names
   -u, --unregistered          Show only unregistered domain names
   -p, --phash                 Render web pages and evaluate visual similarity
   --phash-url URL             Override URL to render the original web page
                               from
   --screenshots DIR           Save web page screenshots into DIR
   -s, --ssdeep                Fetch web pages and compare their fuzzy hashes
                               to evaluate similarity
   --ssdeep-url URL            Override URL to fetch the original web page from
   -t NUMBER, --threads NUMBER
                               Start specified NUMBER of threads (default: 12)
   -w, --whois                 Lookup WHOIS database for creation date
   --tld FILE                  Swap TLD for the original domain from FILE
   --nameservers LIST          DNS or DoH servers to query (separated with
                               commas)
   --useragent STRING          User-Agent STRING to send with HTTP requests
                               (default: Mozilla/5.0 (linux 64-bit)
                               dnstwist/20221022)
   --debug                     Display debug messages
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
