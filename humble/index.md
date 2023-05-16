---
Title: humble
Homepage: https://github.com/rfc-st/humble
Repository: https://gitlab.com/kalilinux/packages/humble
Architectures: all
Version: 1.23-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### humble
 
  This package contains an  humble, and fast, security-oriented HTTP headers
  analyzer.
 
 **Installed size:** `138 KB`  
 **How to install:** `sudo apt install humble`  
 
 {{< spoiler "Dependencies:" >}}
 * publicsuffix
 * python3
 * python3-colorama
 * python3-fpdf
 * python3-requests
 * python3-tldextract
 {{< /spoiler >}}
 
 ##### humble
 
 
 ```
 root@kali:~# humble -h
 usage: humble.py [-h] [-a] [-b] [-g] [-l {es}] [-o {html,pdf,txt}] [-r]
                  [-u URL] [-v]
 
 humble (HTTP Headers Analyzer) - https://github.com/rfc-st/humble
 
 options:
   -h, --help         show this help message and exit
   -a                 Show statistics of the analysis performed on the
                      specified URL.
   -b                 Show a brief analysis; if omitted, a detailed analysis
                      will be shown.
   -g                 Show guidelines on securing most used web
                      servers/services.
   -l {es}            Displays the analysis in the indicated language; if
                      omitted, English will be used.
   -o {html,pdf,txt}  Save analysis to file (URL_yyyymmdd.ext).
   -r                 Show HTTP response headers and a detailed analysis.
   -u URL             URL to analyze, with schema. E.g., https://google.com
   -v, --version      show version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
