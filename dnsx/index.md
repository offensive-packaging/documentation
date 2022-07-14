---
Title: dnsx
Homepage: https://github.com/projectdiscovery/dnsx
Repository: https://gitlab.com/kalilinux/packages/dnsx
Architectures: any
Version: 1.0.7-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dnsx
 
  This package contains a fast and multi-purpose DNS toolkit allow to run
  multiple probes using retryabledns library, that allows you to perform
  multiple DNS queries of your choice with a list of user supplied resolvers,
  additionally supports DNS wildcard filtering like shuffledns
  (https://github.com/projectdiscovery/shuffledns).
   
  Features
   * Simple and Handy utility to query DNS records
   * Supports A, AAAA, CNAME, PTR, NS, MX, TXT, SOA
   * Supports DNS Status Code probing
   * Supports DNS Tracing
   * Handles wildcard subdomains in automated way.
   * Stdin and stdout support to work with other tools.
 
 **Installed size:** `9.16 MB`  
 **How to install:** `sudo apt install dnsx`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dnsx
 
 
 ```
 root@kali:~# dnsx -h
 dnsx is a fast and multi-purpose DNS toolkit allow to run multiple probes using retryabledns library.
 
 Usage:
   dnsx [flags]
 
 Flags:
 INPUT:
    -l, -list string  File input with list of sub(domains)/hosts
 QUERY:
    -a      Query A record (default)
    -aaaa   Query AAAA record
    -cname  Query CNAME record
    -ns     Query NS record
    -txt    Query TXT record
    -ptr    Query PTR record
    -mx     Query MX record
    -soa    Query SOA record
 FILTERS:
    -resp               Display DNS response
    -resp-only          Display DNS response only
    -rcode, -rc string  Display DNS status code (eg. -rcode noerror,servfail,refused)
 RATE-LIMIT:
    -t, -c int            Number of concurrent threads to use (default 100)
    -rl, -rate-limit int  Number of DNS request/second (disabled as default) (default -1)
 OUTPUT:
    -o, -output string  File to write output
    -json               Write output in JSONL(ines) format
 DEBUG:
    -silent       Show only results in the output
    -v, -verbose  Verbose output
    -raw, -debug  Display RAW DNS response
    -stats        Display stats of the running scan
    -version      Show version of dnsx
 OPTIMIZATION:
    -retry int                Number of DNS retries (default 1)
    -hf, -hostsfile           Parse system host file
    -trace                    Perform DNS trace
    -trace-max-recursion int  Max recursion for dns trace (default 32767)
    -flush-interval int       Flush interval of output file (default 10)
    -resume                   Resume
 CONFIGURATIONS:
    -r, -resolver string          List of resolvers (file or comma separated)
    -wt, -wildcard-threshold int  Wildcard Filter Threshold (default 5)
    -wd, -wildcard-domain string  Domain name for wildcard filtering (other flags will be ignored)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
