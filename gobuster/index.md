---
Title: gobuster
Homepage: https://github.com/OJ/gobuster
Repository: https://salsa.debian.org/pkg-security-team/gobuster
Architectures: any
Version: 3.5.0-1
Metapackages: kali-linux-everything kali-linux-large 
Icon: images/gobuster-logo.svg
PackagesInfo: |
 ### gobuster
 
  Gobuster is a tool used to brute-force: URIs (directories and files) in
  web sites, DNS subdomains (with wildcard support), Virtual Host names
  on target web servers, Open Amazon S3 buckets, Open Google Cloud buckets
  and TFTP servers.
   
  Gobuster is useful for pentesters, ethical hackers and forensics experts.
  It also can be used for security tests.
 
 **Installed size:** `7.53 MB`  
 **How to install:** `sudo apt install gobuster`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gobuster
 
 Directory/file & DNS busting tool written in Go
 
 ```
 root@kali:~# gobuster -h
 Usage:
   gobuster [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   dir         Uses directory/file enumeration mode
   dns         Uses DNS subdomain enumeration mode
   fuzz        Uses fuzzing mode. Replaces the keyword FUZZ in the URL, Headers and the request body
   gcs         Uses gcs bucket enumeration mode
   help        Help about any command
   s3          Uses aws bucket enumeration mode
   tftp        Uses TFTP enumeration mode
   version     shows the current version
   vhost       Uses VHOST enumeration mode (you most probably want to use the IP address as the URL parameter)
 
 Flags:
       --delay duration    Time each thread waits between requests (e.g. 1500ms)
   -h, --help              help for gobuster
       --no-color          Disable color output
       --no-error          Don't display errors
   -z, --no-progress       Don't display progress
   -o, --output string     Output file to write results to (defaults to stdout)
   -p, --pattern string    File containing replacement patterns
   -q, --quiet             Don't print the banner and other noise
   -t, --threads int       Number of concurrent threads (default 10)
   -v, --verbose           Verbose output (errors)
   -w, --wordlist string   Path to the wordlist
 
 Use "gobuster [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/102166.js" id="asciicast-102166" async></script>

## gobuster Usage Examples

Scan a website (`-u http://192.168.0.155/`) for directories using a wordlist (`-w /usr/share/wordlists/dirb/common.txt`) and print the full URLs of discovered paths (`-e`):

```
root@kali:~# gobuster -e -u http://192.168.0.155/ -w /usr/share/wordlists/dirb/common.txt

Gobuster v1.2                OJ Reeves (@TheColonial)
=====================================================
[+] Mode         : dir
[+] Url/Domain   : http://192.168.0.155/
[+] Threads      : 10
[+] Wordlist     : /usr/share/wordlists/dirb/common.txt
[+] Status codes : 301,302,307,200,204
[+] Expanded     : true
=====================================================
http://192.168.0.155/blog (Status: 301)
http://192.168.0.155/index.html (Status: 200)
http://192.168.0.155/index (Status: 200)
http://192.168.0.155/photo (Status: 301)
http://192.168.0.155/wordpress (Status: 301)
=====================================================
```
