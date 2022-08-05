---
Title: nikto
Homepage: https://github.com/sullo/nikto
Repository: https://gitlab.com/kalilinux/packages/nikto
Architectures: all
Version: 1:2.1.6+git20190310-0kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability kali-tools-web 
Icon: images/nikto-logo.svg
PackagesInfo: |
 ### nikto
 
  Nikto is a pluggable web server and CGI scanner written in Perl, using
  rfp's LibWhisker to perform fast security or informational checks.
   
  Features:
   - Easily updatable CSV-format checks database
   - Output reports in plain text or HTML
   - Available HTTP versions automatic switching
   - Generic as well as specific server software checks
   - SSL support (through libnet-ssleay-perl)
   - Proxy support (with authentication)
   - Cookies support
 
 **Installed size:** `2.38 MB`  
 **How to install:** `sudo apt install nikto`  
 
 {{< spoiler "Dependencies:" >}}
 * libnet-ssleay-perl
 * perl
 {{< /spoiler >}}
 
 ##### nikto
 
 Scan web server for known vulnerabilities
 
 ```
 root@kali:~# nikto -h
 
        -config+            Use this config file
        -Display+           Turn on/off display outputs
        -dbcheck            check database and other key files for syntax errors
        -Format+            save file (-o) format
        -Help               Extended help information
        -host+              target host/URL
        -id+                Host authentication to use, format is id:pass or id:pass:realm
        -list-plugins       List all available plugins
        -output+            Write output to this file
        -nossl              Disables using SSL
        -no404              Disables 404 checks
        -Plugins+           List of plugins to run (default: ALL)
        -port+              Port to use (default 80)
        -root+              Prepend root value to all requests, format is /directory
        -ssl                Force ssl mode on port
        -Tuning+            Scan tuning
        -timeout+           Timeout for requests (default 10 seconds)
        -update             Update databases and plugins from CIRT.net
        -Version            Print plugin and database versions
        -vhost+             Virtual host (for Host header)
    		+ requires a value
 
 	Note: This is the short help output. Use -H for full help text.
 
 ```
 
 - - -
 
 ##### replay.pl
 
 
 ```
 root@kali:~# replay.pl -h
 replay.pl -- Replay a saved scan result
      -file 		Parse request from this file
      -proxy		Send request through this proxy (format: host:port)
      -help		Help output
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Nikto Usage Example

```root@kali:~# nikto -Display 1234EP -o report.html -Format htm -Tuning 123bde -host 192.168.0.102
- Nikto v2.1.6
---------------------------------------------------------------------------
+ Target IP:          192.168.0.102
+ Target Hostname:    192.168.0.102
+ Target Port:        80
+ Start Time:         2018-03-23 10:49:04 (GMT0)
---------------------------------------------------------------------------
+ Server: Apache/2.2.22 (Ubuntu)
+ Server leaks inodes via ETags, header found with file /, inode: 287, size: 11832, mtime: Fri Feb  2 15:27:56 2018
+ The anti-clickjacking X-Frame-Options header is not present.
+ The X-XSS-Protection header is not defined. This header can hint to the user agent to protect against some forms of XSS
+ The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ "robots.txt" contains 1 entry which should be manually viewed.
+ Uncommon header 'tcn' found, with contents: list
+ Apache mod_negotiation is enabled with MultiViews, which allows attackers to easily brute force file names. See http://www.wisec.it/sectou.php?id=4698ebdc59d15. The following alternatives for 'index' were found: index.html
+ Apache/2.2.22 appears to be outdated (current is at least Apache/2.4.12). Apache 2.0.65 (final release) and 2.2.29 are also current.
+ Allowed HTTP Methods: GET, HEAD, POST, OPTIONS
+ 371 requests: 0 error(s) and 9 item(s) reported on remote host
+ End Time:           2018-03-23 10:50:44 (GMT0) (100 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested
root@kali:~#
root@kali:~# firefox report.html
```
