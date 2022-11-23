---
Title: chkrootkit
Homepage: http://www.chkrootkit.org/
Repository: https://salsa.debian.org/pkg-security-team/chkrootkit
Architectures: any
Version: 0.55-4
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics 
Icon: images/chkrootkit-logo.svg
PackagesInfo: |
 ### chkrootkit
 
  The chkrootkit security scanner searches for signs that the system is
  infected with a 'rootkit'. Rootkits are a form of malware that seek
  to exploit security flaws to grant unauthorised access to a
  computer or its services, generally for malicious purposes.
   
  chkrootkit can identify signs of over 70 different rootkits (see the
  project's website for a list).
   
  Please note that an automated tool like chkrootkit can never
  guarantee a system is uncompromised. Nor does every report always
  signify a genuine problem: human judgement and further investigation
  will always be needed to assure the security of your system.
 
 **Installed size:** `922 KB`  
 **How to install:** `sudo apt install chkrootkit`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### chklastlog
 
 Check lastlog file for deleted entries
 
 
 - - -
 
 ##### chkrootkit
 
 Scan the system for signs of rootkits
 
 ```
 root@kali:~# chkrootkit -h
 Usage: /usr/sbin/chkrootkit [options] [test ...]
 Options:
         -h                show this help and exit
         -V                show version information and exit
         -l                show available tests and exit
         -d                debug
         -q                quiet mode
         -x                expert mode
         -e 'FILE1 FILE2'  exclude files/dirs from results. Must be followed by a space-separated list of files/dirs.
                           Read /usr/share/doc/chkrootkit/README.FALSE-POSITIVES first.
         -s REGEXP         filter results of sniffer test through 'grep -Ev REGEXP' to exclude expected
                           PACKET_SNIFFERs. Read /usr/share/doc/chkrootkit/README.FALSE-POSITIVES first.
         -r DIR            use DIR as the root directory
         -p DIR1:DIR2:DIRN path for the external commands used by chkrootkit
         -n                skip NFS mounted dirs
 ```
 
 - - -
 
 ##### chkwtmp
 
 Check wtmp file deleted entries
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
